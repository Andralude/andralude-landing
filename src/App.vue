<script setup lang="ts">
  import Header from './components/Header.vue';
  import Hero from './components/Hero.vue';
  import Tiles from './components/Tiles.vue';
  import Services from './components/Services.vue';
  import About from './components/About.vue';
  import Contact from './components/Contact.vue';
  import Footer from './components/Footer.vue';
</script>

<script lang="ts">
const url = new URL(window.location.href); 
const pathname = url.pathname;
if (pathname === '/train-annot') {
  window.location.href = 'https://train-annot.spacegamers.fr';
}
</script>

<template>
  <body class="leading-normal tracking-normal text-white gradient" style="font-family: 'Source Sans Pro', sans-serif;">
    <Header />
    <Hero />
    <Tiles />
    <Services />
    <About />
    <Contact />
    <Footer />
  </body>
</template>

<style>
  .gradient {
    background: linear-gradient(90deg, #ff9849 0%, #ab58ff 100%);
  }
</style>