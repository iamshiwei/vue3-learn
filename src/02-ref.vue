<script setup>
import { reactive, ref } from 'vue';

const state = reactive({
  count: 0
})
const setCount = () => {
  count.value++
}
const count = ref(0)
</script>
<template>
  <div>
    <button @click="setCount">{{ state.count }}</button>
    <button @click="setCount">{{ count }}</button>
  </div>
</template>