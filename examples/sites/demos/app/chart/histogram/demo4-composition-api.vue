<template>
  <div>
    <tiny-chart-histogram :data="chartData" :settings="chartSettings"></tiny-chart-histogram>
  </div>
</template>

<script setup lang="jsx">
// 因为柱状图内使用了折线图，使用前需先引入对应模块
import { ref } from 'vue'
import 'echarts/lib/chart/line'
import { ChartHistogram as TinyChartHistogram } from '@opentiny/vue'

const chartData = ref({
  columns: ['日期', '访问用户', '下单用户', '下单率'],
  rows: [
    { 日期: '1/1', 访问用户: 1393, 下单用户: 1093, 下单率: 0.32 },
    { 日期: '1/2', 访问用户: 3530, 下单用户: 3230, 下单率: 0.26 },
    { 日期: '1/3', 访问用户: 2923, 下单用户: 2623, 下单率: 0.76 },
    { 日期: '1/4', 访问用户: 1723, 下单用户: 1423, 下单率: 0.49 },
    { 日期: '1/5', 访问用户: 3792, 下单用户: 3492, 下单率: 0.323 },
    { 日期: '1/6', 访问用户: 4593, 下单用户: 4293, 下单率: 0.78 }
  ]
})
// 柱状图+折线图
const chartSettings = ref({
  showLine: ['下单用户']
})
</script>
