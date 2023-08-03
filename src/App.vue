<script setup>
import { onMounted } from 'vue';

// 生命周期：是可以执行多次的，按照顺序执行
onMounted(() => {
  console.log("mounted");
})
onMounted(() => {
  console.log("mounted2");
})
</script>
<template>
  <div></div>
</template>