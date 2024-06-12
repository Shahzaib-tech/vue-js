<template>
    <h1 class="text-4xl md:text-6xl font-extrabold text-center text-blue-700 my-8 md:my-16">
      Hello from the about Page
    </h1>
    <div>{{ data }}</div>
  </template>
  <script>
export default {
  async asyncData() {
    const { data } = await useFetch('/api/api?name=mario');
    return { data };
  }
};
</script>