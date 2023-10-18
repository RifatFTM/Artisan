<template>
  <div>
    <div>
      <apexchart
        style="width: 100%"
        height="280px"
        type="bar"
        :options="options"
        :series="options.series"
      ></apexchart>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import VueApexCharts from "vue3-apexcharts";
export default defineComponent({
  name: "ProductSold",
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {
      options: {
        series: [
          { name: "Axe", data: [44, 55, 41, 67, 22, 43] },
          { name: "Dove", data: [13, 23, 20, 8, 13, 27] },
          { name: "Persil", data: [11, 17, 15, 15, 21, 14] },
          { name: "Comfort", data: [21, 7, 25, 13, 22, 8] },
          { name: "Simple", data: [21, 7, 25, 13, 22, 8] },
        ],
        chart: {
          type: "bar",

          stacked: true,
        },

        plotOptions: {
          bar: {
            horizontal: false,
            columnWidth: "50%",
            dataLabels: {
              total: {
                enabled: true,
                style: {
                  fontSize: "13px",
                  fontWeight: 900,
                },
              },
            },
          },
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
          ],
        },
        legend: {
          position: "bottom",
          offsetY: 10,
        },
      },
    };
  },
});
</script>

<style scoped></style>
