<template>
  <div>
    <tiny-radio v-model="value" label="1">选项一</tiny-radio>
    <tiny-radio v-model="value" label="2" text="选项二"></tiny-radio>
  </div>
</template>

<script lang="jsx">
import { Radio } from '@opentiny/vue'

export default {
  components: {
    TinyRadio: Radio
  },
  data() {
    return {
      value: '1'
    }
  }
}
</script>
