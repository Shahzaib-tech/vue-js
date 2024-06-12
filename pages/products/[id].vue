<template>
    <Head>
        <Title>
            {{ product.title }}
        </Title>
    </Head>
    <div class="container mx-auto px-4 py-8">
      <div class="bg-white shadow-md p-6 rounded-lg">
        <div class="flex flex-col md:flex-row items-center md:items-start">
          <img :src="product.image" alt="Product Image" class="w-full md:w-1/2 rounded-lg md:mb-0">
          <div class="md:ml-4 md:w-1/2">
            <p class="text-3xl font-bold text-gray-800 mb-4">{{ product.title }}</p>
            <p class="text-lg text-gray-600 mb-4">Price: ${{ product.price }}</p>
            <p class="text-sm text-gray-500 mb-4">ID: {{ product.id }}</p>
            <p class="text-gray-700">{{ product.description }}</p>
            <button class="bg-blue-500 text-white px-4 py-2 rounded-md mt-4 hover:bg-blue-600 focus:outline-none focus:ring focus:ring-blue-300"><i class="material-icons mr-2">add_shopping_cart</i>Add to Cart
</button>
          </div>
        </div>
      </div>
    </div>
  </template>

<script lang="ts" setup>
 definePageMeta({
      layout:'products'
  })
const {id}=useRoute().params
const uri='https://fakestoreapi.com/products/'+id
const {data:product}=await useFetch(uri)
</script>

<style scoped>
img{
    max-width: 400px;
}
</style>