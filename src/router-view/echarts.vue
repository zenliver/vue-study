<!-- ECharts学习 -->
<template lang="html">
  <div id="echarts_study">
    <VeLine :data="chartData" :settings="chartSettings" :extend="extend"></VeLine>
  </div>
</template>

<script>
  import VeLine from 'v-charts/lib/line.common.js';

  export default {
    components: {
      VeLine
    },
    data () {
      return {
        chartSettings: {
          dimension: ['日期'],
          metrics: ['销售量','成交额','成交率'],
          axisSite: {
            right: ['成交率']
          },
          yAxisType: ['KMB','percent'],
          yAxisName: ['额度','百分比'],
          area: true,
        },
        extend: {
          'xAxis.0.axisLabel.rotate': 45
        },
        chartData: {
          columns: ['日期','销售量','成交额','成交率'],
          rows: [
            {
              '日期': '1月1日',
              '销售量': 24242,
              '成交额': 242420,
              '成交率': 0.25
            },
            {
              '日期': '1月2日',
              '销售量': 235255,
              '成交额': 2352550,
              '成交率': 0.36
            },
            {
              '日期': '1月3日',
              '销售量': 74942,
              '成交额': 749420,
              '成交率': 0.31
            },
            {
              '日期': '1月4日',
              '销售量': 54242,
              '成交额': 542420,
              '成交率': 0.18
            }
          ],
        },
      };
    },
    methods: {

    },
    mounted () {

    },
  }
</script>

<style lang="scss" scoped>
  #echarts_study {
    width: 800px;
    margin: 0 auto;
  }
</style>
