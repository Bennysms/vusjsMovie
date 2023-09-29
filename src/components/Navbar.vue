<script setup>
import { RouterLink } from "vue-router";
</script>


<template>
  <header class="max-w-7xl mx-auto py-6 flex items-center justify-between px-5 border-b-2 border-[rgb(78,176,124)]">

    <h1 class="font-bold text-3xl"><span class="text-[rgb(78,176,124)]">Vue</span> Movies</h1>

    <nav class="hidden md:flex gap-5 text-md font-semibold text-[rgb(78,176,124)]">
      <router-link to="/" class="py-2 px-4 bg-[rgb(78,176,124)] text-white rounded-full border-2 border-transparent hover:border-[rgb(78,176,124)] hover:bg-transparent hover:text-[rgb(78,176,124)] transition-all duration-300"
        >Home</router-link
      >
      <router-link to="/about" class="py-2 px-4 bg-[rgb(78,176,124)] text-white rounded-full border-2 border-transparent hover:border-[rgb(78,176,124)] hover:bg-transparent hover:text-[rgb(78,176,124)] transition-all duration-300"
        >About Us</router-link
      >
    </nav>
  </header>
</template>



<style>
    .router-link-active{
        border: 2px solid rgb(78,176,124);
        color : rgb(78,176,124);
        background-color : transparent;
    }
</style>