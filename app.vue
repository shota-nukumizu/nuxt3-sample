<template>
  <h2>{{ organization.login }}</h2>
  <p>{{ organization.description }}</p>
</template>

<script>
export default defineComponent({
  async setup() {
    const [{ data: organization }, { data: repos }] = await Promise.all([
      useFetch(`https://api.github.com/orgs/nuxt`),
      useFetch(`https://api.github.com/orgs/nuxt/repos`)
    ])

    return {
      organization,
      repos
    }
  }
})
</script>