<template>
  <ul>
    <li v-for="colum in list" :key="colum.id">
      <img :src="colum.avatar" :alt="colum.title">
      <h5>{{colum.title}}</h5>
      <p>{{colum.description}}</p>
      <a href="#">進入專欄</a>
    </li>
  </ul>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'
export interface ColumnProps{
    id: number;
    title: string;
    avatar: string;
    description: string;
}

export default defineComponent({
  name: 'ColumnList',
  props: {
    list: {
      type: Array as PropType<ColumnProps[]>,
      required: true
    }
  }
})
</script>
