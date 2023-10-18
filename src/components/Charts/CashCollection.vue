<template>
  <div>
    <div>
      <div>
        <apexchart
          width="100%"
          height="300px"
          type="area"
          :options="options"
          :series="series"
        ></apexchart>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import VueApexCharts from "vue3-apexcharts";
export default defineComponent({
  name: "CashCollection",
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {
      options: {
        chart: {
          id: "vuechart-example",
        },
        xaxis: {
          type: "datetime",
        },
      },
      series: [
        {
          name: "Cash Flow",
          data: [
            { x: new Date("2023-10-01").getTime(), y: 20000 },
            { x: new Date("2023-10-02").getTime(), y: 25000 },
            { x: new Date("2023-10-03").getTime(), y: 22000 },
            { x: new Date("2023-10-04").getTime(), y: 21500 },
            { x: new Date("2023-10-05").getTime(), y: 26000 },
            { x: new Date("2023-10-06").getTime(), y: 25000 },
            { x: new Date("2023-10-07").getTime(), y: 27500 },
            { x: new Date("2023-10-08").getTime(), y: 28000 },
            { x: new Date("2023-10-09").getTime(), y: 25000 },
            { x: new Date("2023-10-10").getTime(), y: 24000 },
            { x: new Date("2023-10-11").getTime(), y: 21000 },
            { x: new Date("2023-10-12").getTime(), y: 27000 },
            { x: new Date("2023-10-13").getTime(), y: 20000 },
          ],
        },
      ],
    };
  },
});
</script>

<style scoped></style>
