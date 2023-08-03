<!-- <script setup>
import { ref, watch } from 'vue';

const count = ref(0)
const setCount = () => {
  count.value++
}

// watch中ref对象不需要加.value
watch(count, (newVal, oldVal) => {
  console.log('count的值发生变化了');
  console.log(newVal);
  console.log(oldVal);
})
</script> -->
<script setup>
import { ref, watch } from 'vue';

const count = ref(0)
const changeCount = () => {
  count.value++
}
const name = ref('cp')
const changeName = () => {
  name.value = 'pc'
}
watch([count, name], ([newCount, newName], [oldCount, oldName]) => {
  console.log(newCount, oldCount);
  console.log(newName, oldName);
}, {
  immediate: true,
  deep: true
})
</script>
<template>
  <div>
    <!-- <button @click="setCount">{{ count }}</button> -->
    <button @click="changeCount">{{ count }}</button>  <br>
    <button @click="changeName">{{ name }}</button>
  </div>
</template>