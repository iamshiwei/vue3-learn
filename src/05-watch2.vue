<script setup>
import { ref, watch } from 'vue';

  const state = ref({count: 0})
  const changeCount = () => {
    state.value.count++
  }
  // 不加deep不会监听count变化,监听全部对象会产生浪费，因为改变对象可能会有多个值
  watch(state, ()=> {
    console.log("count发生变化");
  },{
    // deep有性能损耗，尽量不开启
    deep: true
  })
</script>
<template>
<div>
  <button @click="changeCount">{{ state.count }}</button>
</div>
</template>