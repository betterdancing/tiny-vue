<template>
  <tiny-action-menu :options="options" text-field="name"> </tiny-action-menu>
</template>

<script setup lang="jsx">
import { ref } from 'vue'
import { ActionMenu as TinyActionMenu } from '@opentiny/vue'

const options = ref([
  {
    name: '远程登陆'
  },
  {
    name: '开机'
  },
  {
    name: '关机'
  },
  {
    name: '重启'
  },
  {
    name: '网络设置',
    children: [{ name: '更改安全组' }, { name: '切换VPC', divided: true }]
  }
])
</script>
