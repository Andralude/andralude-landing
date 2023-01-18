<template>
  <div class="p-6 flex flex-grow flex-shrink">
    <div class="flex-1 bg-white rounded-t rounded-b-none overflow-hidden shadow py-2 cursor-pointer">
      <div class="text-center w-full font-bold text-xl text-gray-800 px-6">
        {{ title }}
      </div>
      <img :src="icon" class="w-64 mx-auto" />
      <p class="text-center w-full text-gray-800 text-base px-6 mb-1 font-sans -tracking-[.4px]">
        {{ msg }}
      </p>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Tile',
  props: {
    title: String,
    msg: String,
    icon: String
  }
};
</script>