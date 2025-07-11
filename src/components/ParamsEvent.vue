<template>
  <h2>ParamsEvent</h2>
  <button @click="handle">name</button>
</template>

<script>
  export default {
    methods: {
      handle() {
        this.$emit('show', 'xxx', 'yyy');
      }
    }
  }
</script>