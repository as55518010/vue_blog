<template>
  <div class="container">
    <column-list :list="list"/>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import 'bootstrap/dist/css/bootstrap.min.css'
import ColumnList, { ColumnProps } from './components/ColumnList.vue'
const testData: ColumnProps[] = [
  {
    id: 1,
    title: 'test1的專欄',
    description: 'saddsadas',
    avatar: 'https://cdn.mos.cms.futurecdn.net/zJ5DMr39mEbFYAyandCBMj-1200-80.jpg'
  },
  {
    id: 2,
    title: 'test2的專欄',
    description: '專專專專專',
    avatar: 'https://imgix.bustle.com/uploads/image/2020/8/20/6e6407d6-438d-4ad4-b3d6-e18acec04d7e-avatar-tla.jpg?w=350&h=298&auto=format%2Ccompress&cs=srgb&q=70&fit=crop&crop=focalpoint&fp-x=0.5280172413793104&fp-y=0.46551724137931033'
  }
]
export default defineComponent({
  name: 'App',
  components: {
    ColumnList
  },
  setup () {
    return {
      list: testData
    }
  }
})
</script>

<style>
</style>
