<template>
  <div class="content">
    <tiny-button @click="baseClick" :reset-time="0">默认3000ms后自动关闭提示框 </tiny-button>
    <tiny-button @click="successClick" :reset-time="0"> 500ms后自动关闭提示框 </tiny-button>
    <tiny-button @click="errorClick" :reset-time="0"> 5000ms后自动关闭提示框 </tiny-button>
  </div>
</template>

<script>
import { Button } from '@opentiny/vue'

export default {
  components: {
    TinyButton: Button
  },
  methods: {
    baseClick() {
      this.$message('默认3000ms后自动关闭提示框')
    },
    successClick() {
      this.$message({
        message: '500ms后自动关闭提示框',
        status: 'success',
        duration: '500'
      })
    },
    errorClick() {
      this.$message({
        message: '5000ms后自动关闭提示框',
        status: 'error',
        duration: '5000'
      })
    }
  }
}
</script>
