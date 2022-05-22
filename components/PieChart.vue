<template>
  <div>
    <canvas id="pieChart"></canvas>
  </div>
</template>

<script>
import { Chart, registerables } from "chart.js";
import pieChartData from "@/data/data";
export default {
  data() {
    return {
      pieChartData,
    };
  },

  mounted() {
    const ctx = document.getElementById("pieChart");
    Chart.register(...registerables);
    new Chart(ctx, this.pieChartData);
  },
};
</script>
