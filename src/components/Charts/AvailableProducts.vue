<template>
  <div>
    <div>
      <apexchart
        type="bar"
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
  name: "AvailableProducts",
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
              position: "top",
            },
          },
        },
        dataLabels: {
          enabled: true,
          offsetY: -20,
          style: {
            fontSize: "12px",
            colors: ["#333"],
          },
        },
        xaxis: {
          categories: [
            "AXE",
            "DOVE",
            "PERSIL",
            "COMFORT",
            "SIMPLE",
            "TRESEMME",
            "CAMAY",
            "BRU",
            "PEARS",
          ],
          labels: {
            show: true,

            style: {
              fontSize: "11px",
              fontWeight: 600,
            },
          },
        },
        yaxis: {
          title: {
            text: "Quantity (CTN)",
          },
        },
        fill: {
          opacity: 1,
        },
        legend: {
          show: true,
        },
      },
      chartSeries: [
        {
          name: "Quantity (CTN)",
          data: [48, 32, 16, 24, 36, 42, 20, 14, 30],
        },
      ],
    };
  },
});
</script>

<style scoped></style>
