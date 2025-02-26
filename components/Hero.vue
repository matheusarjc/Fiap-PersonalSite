<template>
  <section id="hero" class="relative h-screen flex items-center justify-center bg-cover bg-center">
    <!-- style="background-image: url('/assets/hero-bg.jpg')" -->

    <div class="absolute inset-0 bg-black opacity-60"></div>
    <div class="relative z-10 text-center text-white px-4">
      <h1 class="text-5xl md:text-7xl font-bold mb-4">Hi, there!</h1>
      <p class="text-xl md:text-2xl mb-8">Software Engineer</p>
      <button
        @click="abrirModal"
        class="px-8 py-4 bg-blue-500 hover:bg-blue-600 transition-colors rounded-full text-lg">
        Saiba Mais
      </button>
    </div>
    <Modal v-if="modalAberto" @fechar="modalAberto = false" />
  </section>
</template>

<script setup lang="ts">
import { ref } from "vue";
import Modal from "~/components/Modal.vue";

const modalAberto = ref(false);
const abrirModal = () => {
  modalAberto.value = true;
};
</script>
