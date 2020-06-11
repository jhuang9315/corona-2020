<script>
import { Line } from "vue-chartjs";

export default {
  extends: Line,
  props: {
    chartData: {
      type: Array
    },
    options: {
      type: Object
    }
  },
  mounted() {
    this.renderChart(
      {
        labels: this.chartData.map(d => d.date).reverse(),
        datasets: [
          {
            label: 'Deaths',
            data: this.chartData.map(d => d.total).reverse(),
            borderColor: "#243665",
            pointBorderColor: "#243665",
            pointBackgroundColor: "#243665",
            backgroundColor: "#8BD8BD"
          },
        ]
      },
      this.options
    );
  }
};
</script>
