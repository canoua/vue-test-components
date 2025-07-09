<script setup>
  import Employee from './components/Employee.vue';
</script>

<template>
  <!-- <Employee name="Vasya" surname="Lolkin" age="24"/> -->
  <Employee :arg="[1, 2, 3]"/>
</template>

<style scoped>

</style>
