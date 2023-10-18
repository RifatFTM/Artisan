<template>
  <div>
    <div>
      <apexchart
        type="bar"
        height="260"
        :options="chartOptions"
        :series="chartSeries"
      ></apexchart>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import VueApexCharts from "vue3-apexcharts";
export default defineComponent({
  name: "AxePrice",
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {
      chartOptions: {
        chart: {
          type: "bar",
        },

        plotOptions: {
          bar: {
            horizontal: false,
            columnWidth: "50%",
            dataLabels: {
              enabled: true,
              position: "bottom",
            },
          },
        },
        dataLabels: {
          enabled: true,
          offsetY: 45,
          style: {
            fontSize: "14px",
            colors: ["#fff"],
          },
        },

        stroke: {
          show: true,
          width: 10,
          colors: ["transparent"],
        },
        xaxis: {
          categories: [
            "DEO AER BS APLLO",
            "DEO AER BS DARK TEMPTATION",
            "DEO AER BS BLCK",
            "DEO AER BS MARNE",
            "DEO AER BS MSK",
            "DEO AER BS COLLISION",
            "DEO AER BS BLACK NGHT",
          ],
          labels: {
            show: true,
            trim: true,
            rotate: -45,
            rotateAlways: true,
            style: {
              fontSize: "11px",
              fontWeight: 600,
            },
          },
        },
        yaxis: {
          title: {
            text: "Prices ",
          },
        },
        fill: {
          opacity: 1,
          colors: ["#26A0FC"],
        },
        legend: {
          position: "bottom",
          offsetY: -10,
        },
      },
      chartSeries: [
        {
          name: "Trade Price",
          data: [307, 300, 308, 315, 302, 301, 305],
        },
      ],
    };
  },
});
</script>

<style scoped></style>
