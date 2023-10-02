<script setup>
import Navbar from './Navbar.vue'

</script>

<template>
  <Navbar />
  <header class="bg-[rgb(78,176,124)] max-w-7xl mx-auto h-[300px] sm:h-[500px] p-3 md:p-6">
    <div class="w-full h-full relative">
      <img src="../assets/bg.jpg" class="w-full h-full object-cover" />
      <div class="absolute top-0 right-0 w-[400px] bg-[#1616166f] h-full p-6 pt-14 backdrop-blur-sm text-gray-300 hidden sm:block">
        <h2 class="text-4xl font-bold mb-6">Movie Name</h2>
        <p class="text-justify leading-8 text-md text-gray-300">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur
          distinctio, sapiente sit blanditiis voluptates a suscipit. Facilis,
          inventore optio id nemo assumenda excepturi illo sapiente sequi quas?
          Repudiandae, aperiam cum?
        </p>
        <button class="w-[60px] h-[60px] bg-white  border-[8px] border-[rgb(78,176,124)] rounded-full px-2 mt-5 shadow-[0_20px_50px_rgb(78,176,124)] group hover:scale-90 transition-all duration-300"><font-awesome-icon :icon="['fas', 'play']" class="text-[rgb(78,176,124)] text-xl"/></button>
      </div>
    </div>
  </header>
</template>

<style>
</style>