<template>
  <div>
    User ID: {{ $route.params.id }}<br>
    {{ user }}
  </div>
</template>

<script>
export default {
  async asyncData ({ $axios, params }) {
    const user = await $axios.$get('https://jsonplaceholder.typicode.com/users/' + params.id)
    return { user }
  }
}
</script>
