<script>
import { Line } from "vue-chartjs";

export default {
  extends: Line,
  mounted() {
    this.renderChart(
      {
        labels: [
          "January",
          "February",
          "March",
          "April",
          "May",
          "June",
          "July"
        ],
        datasets: [
          {
            label: "Data Sync",
            data: [2, 10, 5, 9, 0, 6, 20],
            backgroundColor: "transparent",
            borderColor: "rgba(1, 116, 188, 0.50)",
            pointBackgroundColor: "rgba(171, 71, 188, 1)"
          },
          {
            label: "PDG Generation",
            data: [20, 0, 25, 19, 10, 2, 4],
            backgroundColor: "transparent",
            borderColor: "rgba(5, 19, 20, 0.50)",
            pointBackgroundColor: "rgba(171, 71, 188, 1)"
          },
          {
            label: "Email Sender",
            data: [4, 5, 15, 2, 10, 30, 0],
            backgroundColor: "transparent",
            borderColor: "rgba(249, 17, 48, 0.50)",
            pointBackgroundColor: "rgba(20, 5, 7, 1)"
          }
        ]
      },
      {
        responsive: true,
        maintainAspectRatio: false,
        title: {
          display: true,
          text: "PDF Generation"
        }
      }
    );
  }
};
</script>