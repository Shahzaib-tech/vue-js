<template>
    <div class="flex flex-col min-h-screen">
      <header class="bg-blue-500 text-white">
        <nav class="container mx-auto flex items-center justify-between py-4">
          <NuxtLink to="/" class="text-xl font-bold">Project</NuxtLink>
        </nav>
      </header>
      <div class="container mx-auto py-8 flex-grow">
        <slot />
      </div>
      <footer class="bg-blue-500 text-white py-4">
        <ul class="container mx-auto flex justify-center space-x-4">
          <li>
            <NuxtLink to="/" class="hover:text-gray-300">Home</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/about" class="hover:text-gray-300">About</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/products" class="hover:text-gray-300">Products</NuxtLink>
          </li>
        </ul>
      </footer>
    </div>
  </template>
  