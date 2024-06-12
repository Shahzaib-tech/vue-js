<template>
    <div class="bg-white rounded-lg shadow-md overflow-hidden">
      <div class="relative" style="aspect-ratio: 16/9;">
        <img :src="product.image" alt="Product Thumbnail" class="absolute inset-0 w-full h-full object-cover">
      </div>
      <div class="p-4">
        <h3 class="text-xl font-semibold mb-2">{{ product.title }}</h3>
        <p class="text-gray-700 mb-4">{{ product.description }}</p>
        <div class="flex justify-between items-center">
          <p class="text-lg text-gray-900 font-semibold">${{ product.price }}</p>
          <NuxtLink :to="`/products/${product.id}`" class="text-blue-500 font-bold hover:underline">View Details</NuxtLink>
        </div>
      </div>
    </div>
  </template>
<script>
// import { defineProps } from 'vue';

export default {
  props: {
    product: Object
  },
};

</script>
<style scoped>
.bg-white {
  background-color: #f8f9fa;
}
.shadow-md {
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
}
.overflow-hidden {
  overflow: hidden;
}
.font-semibold {
  font-weight: 600;
}
.text-xl {
  font-size: 1.25rem;
}
.text-lg {
  font-size: 1.125rem;
}
.text-gray-700 {
  color: #4b5563;
}
.text-gray-900 {
  color: #333;
}
.text-blue-500 {
  color: #3f83f8;
}
.hover\:underline:hover {
  text-decoration: underline;
}
</style>