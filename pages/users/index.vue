<template>
  <div>
    <h1>Users</h1>
    <ul>
      <li v-for="user of 5" :key="user">
        <a href="#" @click.prevent="$router.push('/users/' + user)">User {{ user }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
//   methods: {
//     userClick (user) {
//       this.$router.push('/users/' + user)
//     }
//   }
}
</script>
