<template>
  <div>
    <div>
      <div>
        <apexchart
          type="bar"
          height="300"
          :options="chartOptions"
          :series="chartSeries"
        ></apexchart>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import VueApexCharts from "vue3-apexcharts";
export default defineComponent({
  name: "SrSales",
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
        xaxis: {
          categories: [
            "Shriful Rahman",
            "Aminur Rahman",
            "Rifat Alam",
            "Adilur Rahman",
            "Shakif Shaharier",
            "Himadri Mondal",
            "Hasibur Rahman",
            "Shariful Rahman Khan mia",
            "Saidur mia",
            "Ashraful Rahman",
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
          offsetX: 20,
        },
        yaxis: {
          title: {
            text: "Sales Amount (CTN)",
            style: {
              fontSize: "10px",
              fontWeight: "bold",
            },
          },
        },
      },
      chartSeries: [
        {
          name: "Sales Amount (CTN)",
          data: [45, 55, 46, 56, 58, 48, 55, 46, 56, 58],
        },
      ],
    };
  },
});
</script>

<style scoped></style>
