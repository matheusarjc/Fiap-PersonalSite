<template>
  <div class="fixed inset-0 flex items-center justify-center bg-black bg-opacity-70 z-50">
    <div class="bg-white rounded-lg p-8 max-w-lg w-full relative">
      <button
        @click="$emit('fechar')"
        class="absolute top-2 right-2 text-gray-700 hover:text-gray-900">
        &times;
      </button>
      <h2 class="text-2xl font-bold mb-4">Sobre Mim</h2>
      <p class="text-gray-700">
        Aqui você pode colocar um texto descrevendo sua trajetória, seus diferenciais e conquistas.
      </p>
    </div>
  </div>
</template>
