<template>
  <div class="demo-input">
    <tiny-input type="textarea" v-model="textarea" autosize></tiny-input>
    <tiny-input type="textarea" v-model="textarea" :autosize="{ minRows: 2, maxRows: 3 }"></tiny-input>
  </div>
</template>

<script setup lang="jsx">
import { ref } from 'vue'
import { Input as TinyInput } from '@opentiny/vue'

const textarea = ref('')
</script>

<style scoped>
.demo-input .tiny-textarea {
  width: 400px;
}
</style>
