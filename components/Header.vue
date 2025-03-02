<template>
  <header class="fixed top-0 left-0 w-full z-50 bg-transparent">
    <div class="container mx-auto flex justify-center items-center py-4 px-6">
      <nav class="hidden md:flex">
        <ul class="flex space-x-8">
          <li>
            <NuxtLink to="#hero" class="text-white hover:text-blue-300" @click="closeMenu"
              >Home</NuxtLink
            >
          </li>
          <li>
            <NuxtLink to="#sobre" class="text-white hover:text-blue-300" @click="closeMenu"
              >About me</NuxtLink
            >
          </li>
          <li>
            <NuxtLink to="#projetos" class="text-white hover:text-blue-300" @click="closeMenu"
              >Projects and Stuff</NuxtLink
            >
          </li>
          <li>
            <NuxtLink to="#contato" class="text-white hover:text-blue-300" @click="closeMenu"
              >Talk to me</NuxtLink
            >
          </li>
        </ul>
      </nav>
      <!-- Mobile Hamburger -->
      <button class="md:hidden text-white focus:outline-none" @click="toggleMenu">
        <svg
          class="w-6 h-6"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16"></path>
        </svg>
      </button>
    </div>
    <!-- Mobile Sidebar Menu -->
    <div v-if="isMenuOpen" class="md:hidden fixed inset-0 z-40">
      <div class="absolute inset-0 bg-black opacity-50" @click="closeMenu"></div>
      <div class="absolute top-0 right-0 w-64 bg-gray-800 h-full p-6">
        <button class="text-white mb-4 focus:outline-none" @click="closeMenu">
          <svg
            class="w-6 h-6"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"></path>
          </svg>
        </button>
        <nav>
          <ul class="space-y-4">
            <li>
              <NuxtLink to="#hero" class="text-white hover:text-blue-300" @click="closeMenu"
                >Home</NuxtLink
              >
            </li>
            <li>
              <NuxtLink to="#sobre" class="text-white hover:text-blue-300" @click="closeMenu"
                >Sobre</NuxtLink
              >
            </li>
            <li>
              <NuxtLink to="#projetos" class="text-white hover:text-blue-300" @click="closeMenu"
                >Projetos</NuxtLink
              >
            </li>
            <li>
              <NuxtLink to="#contato" class="text-white hover:text-blue-300" @click="closeMenu"
                >Contato</NuxtLink
              >
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<script setup lang="ts">
import { ref } from "vue";

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

const closeMenu = () => {
  isMenuOpen.value = false;
};
</script>
