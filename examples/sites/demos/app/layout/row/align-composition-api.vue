<template>
  <tiny-layout class="tiny-layout-align">
    <tiny-row :flex="true" class="margin-bottom10">
      <tiny-col :span="3">
        <div class="col lg">默认</div>
      </tiny-col>
      <tiny-col :span="3">
        <div class="col md">默认</div>
      </tiny-col>
      <tiny-col :span="3">
        <div class="col sm">默认</div>
      </tiny-col>
    </tiny-row>
    <tiny-row :flex="true" align="middle" class="margin-bottom10">
      <tiny-col :span="3">
        <div class="col lg">middle</div>
      </tiny-col>
      <tiny-col :span="3">
        <div class="col md">middle</div>
      </tiny-col>
      <tiny-col :span="3">
        <div class="col sm">middle</div>
      </tiny-col>
    </tiny-row>
    <tiny-row :flex="true" align="bottom" class="margin-bottom10">
      <tiny-col :span="3">
        <div class="col lg">bottom</div>
      </tiny-col>
      <tiny-col :span="3">
        <div class="col md">bottom</div>
      </tiny-col>
      <tiny-col :span="3">
        <div class="col sm">bottom</div>
      </tiny-col>
    </tiny-row>
  </tiny-layout>
</template>

<script setup lang="jsx">
import { Layout as TinyLayout, Row as TinyRow, Col as TinyCol } from '@opentiny/vue'
</script>

<style scoped>
.lg {
  height: 120px;
}

.md {
  height: 80px;
}

.sm {
  height: 40px;
}
</style>
