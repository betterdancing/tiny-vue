<template>
  <div>
    <p class="font-style">未设置属性is-drop-inherit-width，下拉选项默认撑开：</p>
    <tiny-select v-model="value" placeholder="请选择">
      <tiny-option v-for="item in options" :key="item.value" :label="item.label" :value="item.value"> </tiny-option>
    </tiny-select>
    <p class="font-style">设置了属性is-drop-inherit-width，下拉选项跟随输入框宽度：</p>
    <tiny-select v-model="value" placeholder="请选择" is-drop-inherit-width>
      <tiny-option v-for="item in options" :key="item.value" :label="item.label" :value="item.value"> </tiny-option>
    </tiny-select>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { Select as TinySelect, Option as TinyOption } from '@opentiny/vue'

const options = ref([
  {
    value: '选项1',
    label:
      '黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕黄金糕'
  },
  { value: '选项2', label: '双皮奶' },
  { value: '选项3', label: '蚵仔煎' },
  { value: '选项4', label: '龙须面' },
  { value: '选项5', label: '北京烤鸭' }
])
const value = ref('')
</script>

<style scoped>
.font-style {
  font-size: 14px;
  margin: 8px;
}
</style>