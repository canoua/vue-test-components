<template>
  <h2>Испускание события в атрибуте в Vue</h2>
	<button @click="$emit('show', 'xxx', 'yyy')">
		attrEvent
	</button>
</template>

<script>
  export default {
    methods: {
      show() {
        alert('attrEvent')
      }
    }
  }
</script>