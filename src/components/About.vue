<template>
  <div class="bg-white flex lg:flex-row flex-col justify-between gap-8 py-12">
    <div class="container mx-auto px-8 py-8 gap-2 flex-col flex">
      <div>
        <h2 class="w-full my-2 text-5xl font-bold leading-tight text-center text-gray-800">
        À propos de nous
      </h2>
      <div class="w-full mb-4">
          <div class="h-1 mx-auto gradient w-64 opacity-25 my-0 py-0 rounded-t" />
        </div>
        <p class="font-normal text-lg leading-6 text-gray-600 font-sans">
    Nous sommes une équipe de game designers expérimentés, avec plus de 500 créations originales et des dizaines de milliers de joueurs depuis 20 ans.<br />
    Nos activités sont proposées pour le grand public et pour les entreprises, Pour l'événementiel, la communication, le conseil et la formation.<br />
    Maintes fois primés (As d'Or, Concours Lépine, Fondation Jacques Douce, Gobelet et Dé d'Or Boulogne-Billancourt…), nous sommes reconnus pour notre créativité et notre expertise.<br />
</p>
      </div>
      <div class="w-full lg:w-8/12 lg:pt-8 mx-auto">
        <div id="people" class="grid sm:grid-cols-3 grid-cols-1 lg:gap-4 shadow-lg rounded-md">
          <Person name="Éric" role="Game Designer" src="/assets/avatars/neutre.png"/>
          <Person name="Axel" role="Developper" src="/assets/avatars/alopez.png" />
          <Person name="Dominique" role="Sales Manager" src="/assets/avatars/neutre.png"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
  import Person from './Person.vue';
</script>