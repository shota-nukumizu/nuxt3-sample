<template>
  <h1>{{ user.username }}</h1>
</template>

<script>
export default defineComponent({
  async setup() {
    const { data: user } = await Promise.all([
      useFetch(`https://jsonplaceholder.typicode.com/users/1`)
    ])

    return { user }
  }
})
</script>