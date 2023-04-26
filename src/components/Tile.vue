<template>
  <div class="p-6 flex flex-grow flex-shrink">
    <a class="flex-1 bg-white rounded-t rounded-b-none overflow-hidden shadow py-2" :href="link" target="_blank">
      <div class="text-center w-full font-bold text-xl text-gray-800 px-6">
        {{ title }}
      </div>
      <img :src="icon" class="w-64 mx-auto" />
      <p class="text-center w-full text-gray-800 text-base px-6 mb-1 font-sans -tracking-[.4px]">
        {{ msg }}
      </p>
    </a>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Tile',
  props: {
    title: String,
    msg: String,
    icon: String,
    link: String,
  }
};
</script>