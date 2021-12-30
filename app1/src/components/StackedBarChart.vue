<script>

const horizonalLinePlugin = {
  id: "horizontalLine",
  afterDraw: function (chartInstance) {
    var yValue;
    var yScale = chartInstance.scales["y-axis-0"];
    var canvas = chartInstance.chart;
    var ctx = canvas.ctx;
    var index;
    var line;
    var style;

    if (chartInstance.options.horizontalLine) {
      for (
        index = 0;
        index < chartInstance.options.horizontalLine.length;
        index++
      ) {
        line = chartInstance.options.horizontalLine[index];

        if (!line.style) {
          style = "#080808";
        } else {
          style = line.style;
        }

        if (line.y) {
          yValue = yScale.getPixelForValue(line.y);
        } else {
          yValue = 0;
        }
        ctx.lineWidth = 3;

        if (yValue) {
          window.chart = chartInstance;
          ctx.beginPath();
          ctx.moveTo(0, yValue);
          ctx.lineTo(canvas.width, yValue);
          ctx.strokeStyle = style;
          ctx.stroke();
        }

        if (line.text) {
          ctx.fillStyle = style;
          ctx.fillText(line.text, 0, yValue + ctx.lineWidth);
        }
      }
      return;
    }
  },
};
import { HorizontalBar } from "vue-chartjs";
export default {
  extends: HorizontalBar,
  beforeMount() {
    this.addPlugin(horizonalLinePlugin);
  },
  mounted() {
    this.renderChart(
      {
        labels: ["Data"],
        
        datasets: [
          {
            
            barThickness: 20,
            barPercentage: 1,
            // label: "Data Sync",
            backgroundColor: "#f87979",
            data: [40],
          },
          {
            barThickness: 20,
            barPercentage: 1,
            // label: "PDF Generation",
            backgroundColor: "#3D5B96",
            data: [50],
          },
          {
            barThickness: 20,
            barPercentage: 1,
            // label: "Email Sender",
            backgroundColor: "#1EFFFF",
            data: [20],
            
          },
        ],
        
      },
      {
        // responsive: true,
        // maintainAspectRatio: false,
        plugins: {
            legend: false // Hide legend
        },
        scales: {
          xAxes: [
            {
              stacked: true,
              categoryPercentage: 0.5,
              barPercentage: 1,
            },
          ],
          yAxes: [
            {
              stacked: true,
            },
          ],
        },
      }
    );
  },
};
</script>