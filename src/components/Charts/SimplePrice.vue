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
  name: "SimplePrice",
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
            "FACIAL TONER SOOTHING 6X200ML",
            "FC GEL MOSTURSG TUBE UI L 6X150ML",
            "FC GEL REF TBE GBNL L22 6X150ML",
            "HYDRATING LIGHT MOIST 6X125ML",
            "CLEANSING LTN PURIFYING 6X200ML",
            "MISCELLAR WATER (AR)6X400ML",
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
          colors: ["#8B75D7"],
        },
        legend: {
          position: "bottom",
          offsetY: -10,
        },
      },
      chartSeries: [
        {
          name: "Trade Price",
          data: [207, 285, 308, 315, 302, 301],
        },
      ],
    };
  },
});
</script>

<style scoped></style>
