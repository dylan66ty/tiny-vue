<template>
  <div class="demo-split">
    <tiny-split v-model="split2">
      <template #left>
        <div class="demo-split-pane">自定义左面板</div>
      </template>
      <template #trigger>
        <div class="line"></div>
      </template>
      <template #right>
        <div class="demo-split-pane">自定义右面板</div>
      </template>
    </tiny-split>
  </div>
</template>

<script setup lang="jsx">
import { ref } from 'vue'
import { Split as TinySplit } from '@opentiny/vue'

const split2 = ref(0.4)
</script>

<style scoped>
.demo-split {
  height: 200px;
  border: 1px solid #d9d9d9;
  margin-bottom: 20px;
}

.demo-split-pane {
  padding: 10px;
}

.line {
  width: 5px;
  height: 200px;
  background-color: black;
}
</style>
