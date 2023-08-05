<template>
<div>
  我是sonref组件
</div>
</template>

<script setup>
import {ref} from "vue";

// 子组件的属性和方法默认是不开放给父组件的，可以通过defineExpose编译宏制定哪些属性和方法允许访问
const  name = ref('test name')
const setName = () => {
  name.value = 'test new name'
}
defineExpose({name, setName})
</script>

<style scoped>

</style>