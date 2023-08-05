<script setup>
import { inject } from 'vue';

const yeyval = inject('yeye')
const yeye2 = inject('yeye2')
const setCount = inject('set-count')
</script>
<template>
  <div>
    <h3>孙子组件</h3>
    <div>爷爷组件的值: {{ yeyval }}</div>
    <div>爷爷组件的值: {{ yeye2 }}</div>
    <button @click="setCount">修改顶层数据</button>
  </div>
</template>