<template>
  <div>
    <div>
      <apexchart
        type="line"
        height="280"
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
  name: "NewPurchased",
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {
      chartOptions: {
        chart: {
          type: "line",
        },
        legend: {
          offsetY: 8,
        },

        xaxis: {
          type: "datetime",
          categories: [
            "10/01/2023 GMT",
            "10/02/2023 GMT",
            "10/03/2023 GMT",
            "10/04/2023 GMT",
            "10/05/2023 GMT",
            "10/06/2023 GMT",
            "10/07/2023 GMT",
          ],
        },

        yaxis: {
          title: {
            text: "Quantity (CTN)",
          },
        },
        colors: [
          "#26A0FC",
          "#26E7A6",
          "#FEBC3B",
          "#FF6178",
          "#8B75D7",
          "#00BCD4",
          "#FF5252",
          "#009688",
          "#4CAF50",
        ],
      },
      chartSeries: [
        {
          name: "Axe",
          data: [25, 35, 48, 45, 20, 50, 35],
        },
        {
          name: "Dove",
          data: [15, 35, 58, 25, 20, 50, 35],
        },
        {
          name: "Persil",
          data: [35, 15, 40, 32, 11, 30, 55],
        },
        {
          name: "Comfort",
          data: [20, 15, 38, 40, 25, 55, 40],
        },
        {
          name: "Simple",
          data: [35, 40, 25, 10, 30, 44, 32],
        },
        {
          name: "Tresemme",
          data: [38, 42, 28, 10, 32, 46, 38],
        },
        {
          name: "Camay",
          data: [32, 44, 28, 12, 36, 44, 32],
        },
        {
          name: "Bru",
          data: [48, 25, 8, 18, 32, 4, 32],
        },
        {
          name: "Pears",
          data: [50, 44, 24, 14, 36, 44, 32],
        },
      ],
    };
  },
});
</script>

<style scoped></style>
