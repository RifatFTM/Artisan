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
  name: "TopDistrict",
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {
      chartOptions: {
        chart: {
          type: "bar",
          height: 350,
        },
        labels: {},
        plotOptions: {
          bar: {
            horizontal: true,
          },
        },
        xaxis: {
          categories: [
            "Dhaka",
            "Chittagong",
            "Khulna",
            "Mymensingh",
            "Comilla",
          ],
        },
        yaxis: {},
      },
      chartSeries: [
        {
          name: "Sales Amount",
          data: [100000, 50000, 30000, 35000, 40000],
        },
      ],
    };
  },
});
</script>

<style scoped></style>
