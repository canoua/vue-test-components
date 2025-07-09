<template>
   <p>{{ args }}</p>
   <!-- <p>{{ surname }}</p> -->
   <!-- <p>{{ age }}</p> -->
</template>

<script>
  export default {
    props: ['name', 'surname', 'age'],
    data() {
      return {
        args
      }
    }
  }
</script>