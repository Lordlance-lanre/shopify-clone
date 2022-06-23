<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue'
import './assets/tailwind.css'
</script>

<template>
  <div class="bg-amber-400 h-screen">
    <Navbar/>
    <RouterView />
  </div>
</template>

<style>

</style>
