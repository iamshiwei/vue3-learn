<!-- <script>
  export default {
    setup(){
      console.log('setup');
      const message = 'this is message'
      const loadMsg = () => {
        console.log(message);
      }
      return {
        message,
        loadMsg
      }
    },
    beforeCreate() {
      console.log('boforecreate');
    },
  }
</script> -->
<script setup>
  const message = 'this is message'
      const loadMsg = () => {
        console.log(message);
      }
</script>
<template>
  <div>{{ message }}</div>
  <button @click="loadMsg">打印</button>
</template>