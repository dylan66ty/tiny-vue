<!--
 * Copyright (c) 2022 - present TinyVue Authors.
 * Copyright (c) 2022 - present Huawei Cloud Computing Technologies Co., Ltd.
 *
 * Use of this source code is governed by an MIT-style license.
 *
 * THE OPEN SOURCE SOFTWARE IN THIS PRODUCT IS DISTRIBUTED IN THE HOPE THAT IT WILL BE USEFUL,
 * BUT WITHOUT ANY WARRANTY, WITHOUT EVEN THE IMPLIED WARRANTY OF MERCHANTABILITY OR FITNESS FOR
 * A PARTICULAR PURPOSE. SEE THE APPLICABLE LICENSES FOR MORE DETAILS.
 *
 -->

<template>
  <transition name="tiny-zoom-in-top" @after-leave="doDestroy">
    <ul
      class="tiny-dropdown-menu tiny-popper"
      :class="[state.size && `tiny-dropdown-menu--${state.size}`, popperClass]"
      v-show="state.showPopper"
      @mouseenter="handleMouseenter"
      @mouseleave="handleMouseleave"
    >
      <slot>
        <tiny-dropdown-item
          v-for="(item, index) in options"
          :itemData="item"
          :label="item[textField]"
          :key="index"
          :icon="item.icon"
          :disabled="item.disabled"
          :divided="item.divided"
          :tip="item.tip"
          :tip-position="item.tipPosition"
        >
        </tiny-dropdown-item>
      </slot>
    </ul>
  </transition>
</template>

<script lang="ts">
import { renderless, api } from '@opentiny/vue-renderless/dropdown-menu/vue'
import { props, setup, defineComponent } from '@opentiny/vue-common'
import DropdownItem from '@opentiny/vue-dropdown-item'
import '@opentiny/vue-theme/dropdown-menu/index.less'

export default defineComponent({
  components: {
    TinyDropdownItem: DropdownItem
  },
  emits: ['mouseenter', 'mouseleave'],
  props: [
    ...props,
    'visibleArrow',
    'arrowOffset',
    'placement',
    'popperClass',
    'popperAppendToBody',
    'textField',
    'options'
  ],
  setup(props, context) {
    return setup({ props, context, renderless, api })
  }
})
</script>
