<template>
  <tiny-milestone
    :data="milestoneData"
    :milestones-status="statusMap"
    time-field="date"
    name-field="name"
    status-field="progress"
    flag-status-field="progress"
    flag-name-field="title"
    completed-field="completed"
    flag-content-field="describe"
    flag-field="flags"
  ></tiny-milestone>
</template>

<script lang="jsx">
import { Milestone } from '@opentiny/vue'

export default {
  components: {
    TinyMilestone: Milestone
  },
  data() {
    return {
      statusMap: {
        completed: 'var(--ti-common-color-line-active)',
        doing: '#7ED321',
        back: '#f5222d',
        end: '#faad14',
        cancel: '#d9d9d9'
      },
      milestoneData: [
        {
          name: 'POR1',
          date: '2018-9-7',
          progress: 'completed',
          flags: [
            {
              progress: 'completed',
              title: '第一阶段',
              describe: 'flag-content-field' // 设置节点旗子数据中描述对应的字段名，默认为 'content'
            }
          ]
        },
        {
          name: 'POR2',
          date: '2018-9-8',
          progress: 'completed',
          flags: [
            {
              progress: 'back',
              title: '第二阶段',
              describe: 'flag-content-field'
            }
          ]
        },
        {
          name: 'POR3',
          date: '2018-9-10',
          progress: 'doing',
          content: null
        },
        {
          name: 'POR4',
          date: '2018-9-9',
          progress: 'cancel',
          flags: [
            {
              progress: 'back',
              describe: 'flag-content-field',
              title: '第四阶段1'
            },
            {
              progress: 'doing',
              describe: 'flag-content-field',
              title: '第四阶段2'
            }
          ]
        },
        {
          name: 'POR5',
          date: '2018-9-11',
          progress: 'back',
          flags: [
            {
              progress: 'completed',
              describe: 'flag-content-field',
              title: '第五阶段'
            }
          ]
        }
      ]
    }
  }
}
</script>
