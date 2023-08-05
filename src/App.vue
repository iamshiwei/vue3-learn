<template>
<!--  2. 通过ref标识绑定ref对象-->
  <h1 ref="h1Ref">我是dom标签h1</h1>
  <ref-son ref="sonRef"/>
</template>

<script setup>
import RefSon from "@/ref-son.vue";
import {onMounted, ref} from "vue";
// 1. 调用ref函数
const h1Ref = ref(null)
// 3.挂载完毕后才能获取到
onMounted(() => {
  console.log(h1Ref.value)
  console.log(sonRef.value)
})

const sonRef = ref(null)
</script>

<style lang="scss" scoped>

</style>