<script setup>
import { provide, ref } from 'vue';
import son from './son.vue';
// 普通数据
provide('yeye', '来自爷爷的值')
// 响应式数据
const count = ref(0)
setTimeout(() => {
  count.value++
}, 1000)
provide('yeye2', count)

// 传递方法
const setCount = () => {
  count.value = 100
}
provide('set-count', setCount)
</script>
<template>
  <h1>爷爷组件</h1>
  <son />
</template>