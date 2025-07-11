<template>
  <h2>ParamsEvent</h2>
  <button @click="handle">name</button>
</template>

<script>
  export default {
    data() {
      return{
        
      }
    },
    methods: {
      handle() {
        this.$emit('show', 'xxx', 'yyy');
      }
    }
  }
</script>