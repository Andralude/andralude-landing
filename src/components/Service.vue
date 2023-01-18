<template>
  <div class="p-6 flex flex-grow flex-shrink">
    <div class="flex-1 bg-white rounded-t rounded-b-none overflow-hidden shadow py-2">
      <div class="flex flex-wrap no-underline hover:no-underline">
        <div class="text-center w-full font-bold text-xl text-gray-800 px-6">
          {{title}}
        </div>
        <p class="text-justify w-full text-gray-800 text-base px-6 mb-1 font-sans" style="white-space: pre-line; text-justify: distribute;">
          <slot />
        </p>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Service',
  props: {
    title: String,
    msg: String
  }
};
</script>