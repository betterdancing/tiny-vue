<template>
  <div class="split-v-model">
    <tiny-split v-model="split1" trigger-simple collapse-left-top collapse-right-bottom>
      <template #left>
        <div class="demo-split-pane">左面板</div>
      </template>
      <template #right>
        <div class="demo-split-pane">右面板</div>
      </template>
    </tiny-split>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { Split as TinySplit } from '@opentiny/vue'

const split1 = ref(0.5)
</script>

<style scoped>
.split-v-model {
  height: 200px;
  border: 1px solid #d9d9d9;
}

.demo-split-pane {
  padding: 10px;
}
</style>
s
