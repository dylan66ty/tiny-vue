<template>
  <div class="container">
    <tiny-popover
      placement="top-start"
      title="标题"
      :visible-arrow="true"
      width="200"
      trigger="hover"
      content="这是一段内容,这是一段内容,这是一段内容,这是一段内容。"
    >
      <template #reference>
        <tiny-button>有提示箭头</tiny-button>
      </template>
    </tiny-popover>
    <tiny-popover
      placement="top-start"
      title="标题"
      :visible-arrow="false"
      width="200"
      trigger="hover"
      content="这是一段内容,这是一段内容,这是一段内容,这是一段内容。"
    >
      <template #reference>
        <tiny-button>无提示箭头</tiny-button>
      </template>
    </tiny-popover>
  </div>
</template>

<script setup lang="jsx">
import { Popover as TinyPopover, Button as TinyButton } from '@opentiny/vue'
</script>

<style>
.container .reference-wrapper .tiny-button {
  margin: 0 30px;
}
</style>
