<template>
  <div>
    <div>
      <div class="q-mt-md">
        <apexchart
          width="340px"
          type="pie"
          :options="chartOptions"
          :series="chartOptions.series"
        ></apexchart>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import VueApexCharts from "vue3-apexcharts";
export default defineComponent({
  name: "TopSoldProduct",
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {
      chartOptions: {
        series: [44, 55, 66, 43, 22],
        labels: ["AXe", "Dove", "Persil", "Comfort", "Simple"],
        legend: {
          show: true,
          position: "bottom",
        },
        dataLabels: {
          enabled: true,
          style: {
            fontSize: "9px",
          },
        },
      },
    };
  },
});
</script>

<style scoped></style>
