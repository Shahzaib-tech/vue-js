<template>
    <div class="container mx-auto">
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
      <div v-for="p in products" :key="p.id" >
        <ProductCard :product="p" />
      </div>
    </div>
  </div>
  </template>
  <script setup>
  definePageMeta({
      layout:'products'
  })
  useHead({
    title:"All products"
  })
  const {data:products}= await useFetch('https://fakestoreapi.com/products')
  console.log(products,"productss")
</script>