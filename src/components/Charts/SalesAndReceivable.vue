<template>
  <div>
    <div>
      <apexchart
        style="width: 100%"
        height="420px"
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
  name: "SalesAndReceivable",
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {
      options: {
        series: [
          {
            name: "Sales",
            data: [
              35000, 55000, 41000, 67000, 22000, 43000, 35000, 55000, 41000,
              67000, 22000, 43000,
            ],
          },
          {
            name: "Receivable",
            data: [
              13000, 23000, 20000, 8000, 13000, 27000, 13000, 23000, 20000,
              8000, 13000, 27000,
            ],
          },
        ],
        chart: {
          type: "bar",

          stacked: true,
        },

        plotOptions: {
          bar: {
            horizontal: false,
            columnWidth: "40%",
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
            "01/01/2023 GMT",
            "02/01/2023 GMT",
            "03/01/2023 GMT",
            "04/01/2023 GMT",
            "05/01/2023 GMT",
            "06/01/2023 GMT",
            "07/01/2023 GMT",
            "08/01/2023 GMT",
            "09/01/2023 GMT",
            "10/01/2023 GMT",
            "11/01/2023 GMT",
            "12/01/2023 GMT",
          ],
        },
        legend: {
          position: "bottom",
          offsetY: 10,
        },
        colors: ["#00E396", "#FF4560"],
      },
    };
  },
});
</script>

<style scoped></style>
