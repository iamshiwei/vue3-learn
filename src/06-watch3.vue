<script setup>
import { ref, watch } from 'vue';

const state = ref({
  name: 'zhangsan',
  age: 18
})
const changeName = () => {
  state.value.name = 'lisi'
}
const changeAge = () => {
  state.value.age++
}
// 监听具体属性
watch(() => state.value.age, () => {
  console.log("age变了");
})
</script>
<template>
 <div>当前name: {{ state.name }}</div>
 <div>当前age: {{ state.age }}</div>
 <button @click="changeName">修改name</button>
 <button @click="changeAge">修改年龄</button>
</template>