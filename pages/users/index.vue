<template>
  <div>
    <h1>Users</h1>
    <ul>
      <li v-for="user of users" :key="user.id">
        <a href="#" @click.prevent="userClick(user.id)">User {{ user.name }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  async asyncData ({ $axios }) {
    const users = await $axios.$get('https://jsonplaceholder.typicode.com/users')
    return { users }
  },
  methods: {
    userClick (user) {
      // console.log('User click: ', user)
      this.$router.push('/users/' + user)
    }
  }
}
</script>
