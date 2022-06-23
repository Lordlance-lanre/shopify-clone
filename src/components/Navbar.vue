<template>
	<header>
      <nav class="bg-gray-900 text-white md:flex md:justify-between py-3 md:py-2 text-lg">
        <div class="px-5">
          <h1 class="md:text-xl text-xl">Logo</h1>
        </div>

        <div class="hidden px-10 py-1 space-x-5 md:text-lg md:flex">
          <RouterLink to="/" class="hover:text-red-400">Home</RouterLink>
          <RouterLink class="hover:text-red-400" to="/about">About</RouterLink>
          <RouterLink class="hover:text-red-400" to="/services">Services</RouterLink>
          <RouterLink class="hover:text-red-400" to="/contact">Contact</RouterLink>
        </div>

        <div class="md:hidden flex justify-end -mt-7 mx-3">
          <button @click="toggleMenu = !toggleMenu"  class="flex items-center px-1 py-0 border rounded">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
          </svg>
          </button>
        </div>
      </nav>

        <div class="md:hidden terms px-4 py-4 bg-gray-900 text-white transition-all ease-linear h-full w-full delay-1000 duration-500" v-show="toggleMenu">
          <RouterLink to="/" class="hover:text-red-400 block py-1">Home</RouterLink>
          <RouterLink class="hover:text-red-400 py-1 block" to="/about">About</RouterLink>
          <RouterLink class="hover:text-red-400 py-1 block" to="/services">Services</RouterLink>
          <RouterLink class="hover:text-red-400 block" to="/contact">Contact</RouterLink>
        </div>
  </header>
</template>

<script setup>
	import {ref} from 'vue';

  const toggleMenu = ref(false)

</script>

  