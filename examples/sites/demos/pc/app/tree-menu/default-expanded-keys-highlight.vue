<template>
  <div class="tiny-demo">
    <h4>点击改变<tiny-button @click="changeHighlight">highlight</tiny-button></h4>
    <tiny-tree-menu
      node-key="id"
      :data="treeData"
      :default-expanded-keys="expandedKeys"
      :default-expanded-keys-highlight="highlight"
    ></tiny-tree-menu>
  </div>
</template>

<script>
import { TreeMenu, Button } from '@opentiny/vue'

export default {
  components: {
    TinyTreeMenu: TreeMenu,
    TinyButton: Button
  },
  data() {
    return {
      expandedKeys: [20101],
      highlight: 401,
      treeData: [
        {
          id: 100,
          label: '首页'
        },
        {
          id: 200,
          label: '指南',
          children: [
            {
              id: 201,
              label: '引入组件',
              children: [
                { id: 20101, label: '按需引入' },
                { id: 20102, label: '完整引入' }
              ]
            },
            { id: 202, label: '后端适配器' },
            { id: 203, label: '服务代理' },
            { id: 204, label: '构建部署' }
          ]
        },
        {
          id: 300,
          label: '组件',
          children: [
            {
              id: 300,
              label: '组件'
            },
            {
              id: 301,
              label: '表单组件',
              children: [
                {
                  id: 30101,
                  label: 'Button 按钮',
                  url: 'http://his-beta.huawei.com/aurora/#/webcore/v3/zh-CN/component/button'
                },
                { id: 30102, label: 'Datepicker 日期', url: '' },
                { id: 30103, label: 'Dropdown 下拉框', url: '' },
                { id: 30104, label: 'DropTimes 下拉时间', url: '' },
                { id: 30105, label: 'Input 输入框', url: '' }
              ]
            },
            { id: 302, label: '数据组件' },
            { id: 303, label: '导航组件' },
            { id: 304, label: '业务组件' }
          ]
        },
        {
          id: 400,
          label: '教程',
          children: [
            {
              id: 401,
              label: '页面布局',
              children: [
                { id: 40101, label: '添加标签页', url: '' },
                { id: 40102, label: '标签页配置', url: '' }
              ]
            },
            {
              id: 402,
              label: '查询功能',
              children: [
                { id: 40201, label: '添加查询页面', url: '' },
                { id: 40202, label: '列表属性配置', url: '' },
                { id: 40203, label: '通讯录查询', url: '' }
              ]
            },
            {
              id: 403,
              label: '新增功能',
              children: [
                { id: 40301, label: '表单新增功能', url: '' },
                { id: 40302, label: '表单数据验证', url: '' }
              ]
            },
            {
              id: 404,
              label: '编辑功能',
              children: [
                { id: 40401, label: '开启编辑功能', url: '' },
                { id: 40402, label: '保存表格数据', url: '' }
              ]
            }
          ]
        },
        {
          id: 500,
          label: '规范'
        },
        {
          id: 600,
          label: '性能'
        },
        {
          id: 700,
          label: '案例'
        },
        {
          id: 800,
          label: '更新日志'
        }
      ]
    }
  },
  methods: {
    changeHighlight() {
      setTimeout(() => {
        this.highlight = 20101
      }, 100)
    }
  }
}
</script>
