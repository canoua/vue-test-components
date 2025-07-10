<script >
  // import Employee from './components/Employee.vue';
  import User from './components/User.vue';
  export default {
    data() {
      return {
        users: [
          {
            id: 1,
            name: 'name1',
            surn: 'surn1'
          },
          {
            id: 2,
            name: 'name2',
            surn: 'surn2'
          },
          {
            id: 3,
            name: 'name3',
            surn: 'surn3'
          },
        ],
      }
    }
  }
  
</script>

<template>
	<User
		v-for="user in users"
		:name="user.name"
		:surn="user.surn"
		:key="user.id"
	>
    <p>
      {{ user.name }}
    </p>
    <p>
      {{ user.id }}
    </p>
    <p>
      {{ user.surn }}
    </p>  
    <hr>
  </User>
</template>

<style scoped>

</style>
