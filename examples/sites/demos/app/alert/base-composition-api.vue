<template>
  <div>
    <tiny-alert description="type 为默认值 success"></tiny-alert>
    <tiny-alert type="error" description="type 为 error"></tiny-alert>
    <tiny-alert type="info" description="type 为 info"></tiny-alert>
    <tiny-alert type="warning" description="type 为 warning"></tiny-alert>
  </div>
</template>

<script setup lang="jsx">
import { Alert as TinyAlert } from '@opentiny/vue'
</script>
