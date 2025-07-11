<template>
	<h1>Испускание событий</h1>
  <button @click="handleClick">Нажми меня</button>
	<div>
		<h2>Практика</h2>
		<button @click="btn1">btn1</button>
		<button @click="btn2">btn2</button>
	</div>
</template>

<script>
export default {
  methods: {
    handleClick() {
      this.$emit('my-event', { 
				message: 'Событие испущено!' 
			});
    },
		btn1() {
			this.$emit('btn1-event', { 
				message: 'btn1' 
			});
		},
		btn2() {
			this.$emit('btn2-event', { 
				message: 'btn2' 
			});
		}
  }
}
</script>
