<script>
import { HorizontalBar } from "vue-chartjs";

export default {
  extends: HorizontalBar,
  mounted() {
    this.renderChart(
      {
        labels: [
          "January",
          "February",
          "March",
          "April",
          "May"
        ],
        datasets: [
          {
            label: "Data Sync",
            backgroundColor: ['#E74C3C', '#E67E22', '#F1C40F', '#3498DB', '#27AE60'],
            data: [65, 59, 80, 81, 80]
          }
        ]
      },
      { responsive: true, maintainAspectRatio: false }
    );

  }
};
</script>

