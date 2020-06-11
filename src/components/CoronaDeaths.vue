<template>
  <div class="container-xl" data-aos="fade-up" data-aos-anchor="#trigger-left" data-aos-anchor-placement="top-top">
    <line-chart class="graph"
      v-if="arrDeaths.length > 0"
      v-bind:chartData="arrDeaths"
      v-bind:options="chartOptions"
    />
  </div>
</template>

<script>
import axios from "axios";
import moment from "moment";
import LineChart from "./LineChart";

export default {
  components: {
    LineChart
  },
  data() {
    return {
      arrDeaths: [],
      chartOptions: {
        responsive: true,
        maintainAspectRatio: false,
        legend:{display:false},
        elements: {point:{radius: 0}},
        scales: {
          xAxes: [{gridLines: {display:false}}],
          yAxes: [{gridLines: {display:false}}]  
        }
      }
    };
  },
  async created() {
    const { data } = await axios.get("https://covidtracking.com/api/us/daily");

    data.forEach(d => {
      const date = moment(d.date, "YYYYMMDD").format("M/D");
      const {
        death
      } = d;
      this.arrDeaths.push({ date, total: death });
    });
  }
};
</script>

<style scoped>
.graph{
  padding-top:40px;
}
</style>