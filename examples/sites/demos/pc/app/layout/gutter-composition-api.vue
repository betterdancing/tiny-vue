<template>
  <div class="content">
    <tiny-layout>
      <div class="title"></div>
      <tiny-row :gutter="20">
        <tiny-col :span="4">
          <div class="col">gutter 20px</div>
        </tiny-col>
        <tiny-col :span="4">
          <div class="col">gutter 20px</div>
        </tiny-col>
        <tiny-col :span="4">
          <div class="col">gutter 20px</div>
        </tiny-col>
      </tiny-row>
    </tiny-layout>
  </div>
</template>

<script setup>
import { Layout as TinyLayout, Row as TinyRow, Col as TinyCol } from '@opentiny/vue'
</script>

<style scoped>
.tiny-row {
  margin-bottom: 20px;
}

.tiny-row .last-child {
  margin-bottom: 0;
}

.tiny-col .col {
  line-height: 30px;
  text-align: center;
  color: #fff;
  background: #1f9ed8;
  border-radius: 15px;
}

.tiny-col:nth-child(even) .col {
  background: #73d0fc;
}
</style>
