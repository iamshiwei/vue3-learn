<script setup>

// 接收属性
const props =  defineProps({
  message: String ,
  count: Number
})
const emits = defineEmits(['get-message']);
emits('get-message', 'this is son message')
console.log(props);
</script>
<template>
  <div class="son">
    <h3>子组件</h3>
    <h2>父子间信息：{{ message }}---{{ count }}</h2>
  </div>
</template>