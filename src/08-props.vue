<script setup>
import { ref } from 'vue';
import SonCom from './son-com.vue';
const count =ref(100)

const gettMessage = (p) => {
  console.log(p);
}

</script>
<template>
  <div class="son">
    <h3>父组件</h3>
    <!-- 绑定属性 -->
    <SonCom message="father message" :count="count" @get-message="gettMessage"/>
    <button @click="count++">modify cout</button>
  </div>
</template>