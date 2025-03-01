<template>
  <div>
    <Header />
    <main>
      <Hero />
      <Sobre />
      <Projetos />
      <Contato />
    </main>
    <Footer />
  </div>
</template>

<script setup lang="ts">
import Header from "~/components/Header.vue";
import Hero from "~/components/Hero.vue";
import Sobre from "~/components/About.vue";
import Projetos from "~/components/Projects.vue";
import Contato from "~/components/Contact.vue";
import Footer from "~/components/Footer.vue";
import "~/assets/css/global.css";
</script>
