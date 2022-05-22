<template>
  <div>
    <h1 class="text-2xl">{{ text }}</h1>
    <Pie :data="chartData"/>
  </div>
</template>

<script>
import {Pie} from 'vue-chartjs'

const DATA_COUNT = 5;
const NUMBER_CFG = {count: DATA_COUNT, min: 0, max: 100};

export default {
  components: {
    Pie
  },
  data() {
    return {
      text: "Pie chart",
      chartData: {
        labels: ['Red', 'Orange', 'Yellow', 'Green', 'Blue'],
        // datasets: [
        //   {
        //     label: 'Dataset 1',
        //     data: Utils.numbers(NUMBER_CFG),
        //     backgroundColor: Object.values(Utils.CHART_COLORS),
        //   }
        // ]
      }
    }
  }
}
</script>



