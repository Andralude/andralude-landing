<template>
  <div class="p-4 pb-6 flex justify-center flex-col items-center">
    <img class="block object-cover w-32 h-32" :src="src" />
    <p class="font-bold text-xl leading-5 text-gray-800 mt-4">{{name}}</p>
    <p class="font-medium text-xl leading-5 text-gray-800 mt-4">{{role}}</p>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Person',
  props: {
    name: String,
    src: String,
    role: String
  }
};
</script>
