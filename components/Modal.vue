<template>
  <div class="fixed inset-0 flex items-center justify-center bg-black/90 z-50">
    <div class="bg-white rounded-lg p-8 max-w-lg w-full relative">
      <button
        @click="$emit('fechar')"
        class="absolute top-2 right-2 text-gray-700 hover:text-gray-900">
        &times;
      </button>
      <h2 class="text-2xl font-bold mb-4">Fun Fact</h2>
      <p class="text-gray-700">
        In addition to debugging lines of code, I also "debug" the traditional teaching! As CEO of
        <a href="https://skoolab.academy" target="_blank" class="underline">@Skoolab</a>, I not only
        reprogram learning - helping students release their dopamine to transform old methods - but
        also balance the art of software engineering with the adrenaline of leading a fast-paced
        startup. Each bug I solve drives a new innovative insight into the world of education!
      </p>
    </div>
  </div>
</template>
