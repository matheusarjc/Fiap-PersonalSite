<template>
  <section
    id="hero"
    class="relative h-screen flex items-center justify-center bg-cover bg-center"
    style="background-image: url('/assets/hero-bg.jpg')">
    <!-- Camada de sobreposição escura -->
    <div class="absolute inset-0 bg-black opacity-60"></div>

    <!-- Conteúdo principal do Hero -->
    <div class="relative z-10 flex flex-col items-center text-center gap-1.5 text-white px-4">
      <!-- Título -->
      <div>
        <h1 class="text-5xl md:text-7xl font-bold">Hi, there!</h1>
        <h2 class="text-3xl md:text-7xl font-extralight text-left">This is</h2>
      </div>

      <div class="relative">
        <div class="relative top-0">
          <img
            class="w-64 h-64 object-cover rounded-full border-4 border-blue-500 brightness-80 shadow-img"
            src="~/assets/img/profile.jpeg"
            alt="Foto de perfil" />
        </div>
        <div class="absolute right-0 left-0">
          <div class="relative">
            <p
              class="text-4xl md:text-2xl absolute right-14 left-0 bottom-14 italic font-bold text-shadow-custom">
              Matheus
            </p>
            <p
              class="text-4xl md:text-2xl absolute right-0 left-20 bottom-8 italic font-bold text-shadow-custom">
              Araujo
            </p>
          </div>
        </div>
        <p
          class="text-2xl md:text-2xl absolute right-0 left-0 bottom-0 italic font-thin tracking-wider text-shadow-custom-blur underline">
          Software Engineer
        </p>
      </div>
      <div class="flex w-full justify-end">
        <h2 class="text-3xl md:text-7xl font-extralight">introduction.</h2>
      </div>

      <button
        @click="abrirModal"
        class="px-6 py-2 bg-blue-500 hover:bg-blue-600 transition-colors rounded-full text-lg font-medium mt-6">
        Fun Fact
      </button>
    </div>

    <!-- Modal (abre ao clicar em "Saiba Mais") -->
    <!-- Transition para o Modal -->
    <transition
      enter-from-class="opacity-0"
      enter-to-class="opacity-100"
      enter-active-class="transition-opacity duration-300"
      leave-from-class="opacity-100"
      leave-to-class="opacity-0"
      leave-active-class="transition-opacity duration-300">
      <!-- Modal (abre ao clicar em "Fun Fact") -->
      <Modal v-if="modalAberto" @fechar="modalAberto = false" />
    </transition>
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
