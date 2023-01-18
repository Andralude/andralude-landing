<script setup lang="ts">
  import Tile from './Tile.vue';
</script>

<template>
  <section class="bg-white border-b py-8" id="activities">
    <div class="container mx-auto flex flex-wrap pt-4 pb-12">
      <h2 class="w-full my-2 text-5xl font-bold leading-tight text-center text-gray-800">
        Nos activités phares
      </h2>
      <div class="w-full mb-4">
        <div class="h-1 mx-auto gradient w-64 opacity-25 my-0 py-0 rounded-t" />
      </div>
      <div class="grid lg:grid-cols-3 gap-x-8 gap-y-4 lg:mx-20">
        <Tile title="Secret Friend" msg="L'application pour remettre l'humain au centre de votre entreprise" icon="/assets/tiles/secretfriend.svg" />
        <Tile title="Improvisation" msg="Théâtre d'improvisation, catch d'improvisation" icon="/assets/tiles/improvisation.svg" />
        <Tile title="Cinéma interactif" msg="Des films dont vous êtes le heros" icon="/assets/tiles/cinema.svg" />
        <Tile title="Escape Game" msg="Le jeu d'évasion dans la vraie vie" icon="/assets/tiles/escapegame.svg" />
        <Tile title="Jeu de role" msg="Jeux de rôles grandeur nature, soirée d'enquêtes "  icon="/assets/tiles/roleplay.svg" />
        <Tile title="Théâtre immersif" msg="Des comédiens jouent et improvisent sur fond d'une intrigue" icon="/assets/tiles/theatre.svg" />
      </div>
    </div>
  </section>
</template>