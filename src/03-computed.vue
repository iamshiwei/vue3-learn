<script setup>
import { computed, ref } from 'vue';

const list = ref([1,2,3,4,5,6,7,8])
const computedList = computed(() => {
  return list.value.filter(v => v> 3)
})
setTimeout(() => {
  list.value.push(9,10)
}, 1000);
</script>
<template>
  <div>
    原始数据：{{ list }} <br>
    计算数组：{{ computedList }}
  </div>
</template>