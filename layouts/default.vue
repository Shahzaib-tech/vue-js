<template>
    <div class="bg-gray-100 min-h-screen">
      <header class="bg-purple-600 text-white">
        <nav class="container mx-auto flex items-center justify-between py-4">
          <NuxtLink to="/" class="text-xl font-bold">Project</NuxtLink>
          <ul class="flex space-x-4">
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
        </nav>
      </header>
      <div class="container mx-auto py-8">
        <slot />
      </div>
    </div>
  </template>
  