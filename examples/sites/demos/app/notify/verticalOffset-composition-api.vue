<template>
  <div class="content">
    <tiny-button @click="handleClick" :reset-time="0">弹出提示框</tiny-button>
  </div>
</template>

<script setup lang="jsx">
import { Notify, Button as TinyButton } from '@opentiny/vue'

function handleClick() {
  Notify({
    type: 'info',
    title: (h, params) => <h4 style="margin:0">通知消息的标题</h4>,
    message: '通知消息的正文，通知消息的正文，通知消息的正文，通知消息的正文，通知消息的正文，通知消息的正文',
    position: 'top-right',
    duration: 500000,
    customClass: 'my-custom-cls',
    verticalOffset: 100
  })
}
</script>
