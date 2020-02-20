
<template>
  <div>
    <div class="field is-grouped">
      <div class="control">
        <label class="checkbox">
          <input type="checkbox" :value="2017" v-model="selectedYears">
          Existing standards
        </label>
      </div>
      <div class="control">
        <label class="checkbox">
          <input type="checkbox" :value="2018" v-model="selectedYears">
          Replacement Wattage
        </label>
      </div>
    </div>

    <line-chart
      :width="500"
      :height="300"
      :labels="['400W Metal Hyde', '250W Metal Hyde', '2x4 Troffer', '2x2 Troffer', '6-Lamp T5', '4-Lamp T5', '6-Lamp T5']"
      :datasets="displayedDatasets"
      :options="$options.options"
    ></line-chart>
  </div>
</template>

<script>
import numeral from 'numeral';
import LineChart from './LineChart';
const datasets = {
  2017: {
    label: 'Existing Wattage',
    borderColor: 'rgba(50, 115, 220, 0.5)',
    backgroundColor: 'rgba(50, 115, 220, 0.1)',
    data: [458, 285, 128, 366, 224, 192]
  },
  2018: {
    label: 'Typical Replacement Wattage',
    borderColor: 'rgba(255, 56, 96, 0.5)',
    backgroundColor: 'rgba(255, 56, 96, 0.1)',
    data: [180, 80, 48, 30, 150, 100, 100]
  }
};
const options = {
  scales: {
    yAxes: [{
      ticks: {
        beginAtZero: true,
        callback: value => numeral(value).format('$0,0')
      }
    }]
  },
  tooltips: {
    mode: 'index',
    callbacks: {
      label(tooltipItem, data) {
        const label = data.datasets[tooltipItem.datasetIndex].label;
        const value = numeral(tooltipItem.yLabel).format('$0,0');
        return `${label}: ${value}`;
      }
    }
  }
};
export default {
  name: 'Case',
  datasets,
  options,
  components: {
    LineChart
  },
  data() {
    return {
      selectedYears: [2018, 2017]
    };
  },
  computed: {
    displayedDatasets() {
      return this.selectedYears.map(year => datasets[year]);
    }
  }
}
</script>

