<template>
  <h1>Page Visits: {{ data }}</h1>
</template>

<script setup>
const { data } = await useAsyncData('count', () => $fetch('/api/count'))
</script>