<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <div class="col-sm my-3">
          <!-- <img src="./assets/bahl.jpg" id="image" /> -->
          <!-- <img
            alt="bahl logo"
            src="data:image/jpeg;base64,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
            kUMaORlLKoDEaG1+Wg9KKMU7p
            G0aUIu8UiTisMkilHUMp3g7iORHEVlq5tKKkrMtYPZ0MSlI41RT8lRYa33Abt9FFLRGIwjFWSLeE2Ph4m
            Zo4kQt7RUAZt/te9vO/nWFFLYjEacIu6RYTo1gwjIMNCFYhmGRbEjdfThc6btTzrHNwtaxrzFNK2VEjF7J
            glKs8alk0RhoyjkGWxA7r1s4pm0qcZatF1cDGI+qCKI92UCy6m50HM7+d6WVrGckbWtoWo9kwLEYRDH1R3
            x5Rk5+zu361jLG1raGFTilltoe4LZcMJvHGFNst9SQvugnUL3DSsqKQjTjHYiU6gix3Gsm5jB0awYJIw0Vzv
            OQXPjzrTm48CLmKf6USMNsnDxo0aQxqj3zqFAVrixzDjcaa1lRilZI2VOCVktBDsmBIjAsMYiN7plGU333HG
            mWNrW0CpxUcqWhGh6NYNMtsNF2TdbqDY89eXDlwrCpx4GqoU1+VE7D4KNGd0RVaQguwABcjQFjx/wCprZJI3UYptpbSRWTY/9k="

              width="75px"
          /> -->
          <center>
            <b>EStatement Project</b><br><br>
          </center>
        </div>
      </div>
    </div>

<b-container >
  <b-row> 
    <b-col cols="3" ><center>Job Inserter</center><StackedBarChart :height="200" /></b-col>
    <b-col cols="3"><center>Data Sync</center><StackedBarChart :height="200"/></b-col>
    <b-col cols="3"><center>PDF Generation</center><StackedBarChart :height="200"/></b-col>
    <b-col cols="3"><center>Email Sender</center><StackedBarChart :height="200"/></b-col>
  </b-row>
</b-container>

    <div class="container my-5">
      <div class="row">
        <div class="col-sm">
          <br />
          Combined Graph
          <LineChart :height="200"/>
        </div>
        <div class="col-sm">
          <br />
          Combined Graph
          <AreaChart :height="200"/>
        </div>
        <div class="col-sm" id="bar" width="500px">
          Data Sync
          <BarChart :height="200" />
        </div>
        <div class="col-sm">
          KAFKA Messages
          <PieChart :key="componentKey"  :height="200"/>
        </div>
        
        <div class="row">
          <div class="col-sm">
            <br />
            HorizontalBAR
            <HorizontalBar :height="200"/>
          </div>
          <div class="col-sm">
            <br />
            Stacked Bar Chart
            <StackedBarChart :height="200"/>
          </div>
        </div>
      </div>
    </div>
    <GetDAta/>
  </div>
</template>

<script>
import StackedBarChart from "./components/StackedBarChart.vue";
import BarChart from "./components/BarChart.vue";
import AreaChart from "./components/AreaChart.vue";
import PieChart from "./components/PieChart.vue";
import LineChart from "./components/LineChart.vue";
import HorizontalBar from "./components/HorizontalBar.vue";
import GetDAta from './components/GetDAta.vue'
export default {
  name: "App",
  components: {
    BarChart,
    AreaChart,
    PieChart,
    LineChart,
    HorizontalBar,
    StackedBarChart,GetDAta
  },
  methods: {
    forceRerender() {
      this.componentKey += 1;
    },
  },
  data() {
    return {
      componentKey: 0,
      chartOptions: {
        hoverBorderWidth: 20,
      },
      chartData: {
        hoverBackgroundColor: "red",
        hoverBorderWidth: 10,
        labels: ["Green", "Red", "Blue"],
        datasets: [
          {
            label: "Data One",
            backgroundColor: ["#41B883", "#E46651", "#00D8FF"],
            data: [1, 10, 5],
          },
        ],
      },
    };
  },
  created() {
    this.forceRerender();
    this.timer = setInterval(this.forceRerender, 5000);
  },
  mounted() {
    // console.warn("Hello")
    // this.axios({
    //   method: "get",
    //   cors:true,
    //   url: "http://localhost:8080/fruits",
    //   headers: { 'Access-Control-Allow-Origin': true },
    // }).then((data) => console.warn(data.data));
  },
};
</script>
<style>
#radar {
  width: 300px;
}
#bar {
  width: 500px;
}
#line {
  width: 300px;
}
#pie {
  width: 300px;
}
#image {
  width: 50px;
}
</style>