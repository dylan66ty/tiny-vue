<template>
  <div>
    <div id="tiny-loading1" style="width: 100%; margin-bottom: 10px; height: 120px"></div>
    <div id="tiny-loading2" style="width: 100%; margin-bottom: 10px; height: 120px"></div>
    <div id="tiny-loading3" style="width: 100%; margin-bottom: 10px; height: 120px"></div>
  </div>
</template>

<script lang="jsx">
import { Loading } from '@opentiny/vue'

export default {
  data() {
    return {
      loadingInstance: null
    }
  },
  mounted() {
    this.loadingInstance = Loading.service({
      target: document.getElementById('tiny-loading1'),
      size: 'small'
    })
    this.loadingInstance = Loading.service({
      target: document.getElementById('tiny-loading2'),
      size: 'medium'
    })
    this.loadingInstance = Loading.service({
      target: document.getElementById('tiny-loading3'),
      size: 'large'
    })
  }
}
</script>
