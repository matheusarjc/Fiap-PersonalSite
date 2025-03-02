<template>
  <section id="projetos" class="py-20">
    <div class="container mx-auto">
      <h2 class="text-4xl font-bold text-center mb-10">Meus Projetos</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <Project1 />
        <Project1 />
        <Project1 />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import Project1 from "~/components/micro/Project1.vue";
</script>
