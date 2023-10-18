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
            "SH KERATIN SMTH UI P/E 12X700ML",
            "SH SMOOTH & SILKY 6X828ML",
            "CD LUXRS MSTRE SMTH SLK 6X828ML",
            "CD LUXRS MSTRE MST RCH 6X828ML",
            "SH COLOR REVITALIZE 6X828ML",
            "SH 24HR VLUME ANTI-BRKG 6X828ML",
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
          colors: "#00BCD4",
        },
        legend: {
          position: "bottom",
          offsetY: -10,
        },
      },
      chartSeries: [
        {
          name: "Trade Price",
          data: [407, 485, 408, 415, 402, 401],
        },
      ],
    };
  },
});
</script>

<style scoped></style>
