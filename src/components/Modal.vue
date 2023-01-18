<template>
  <!-- Modal -->
  <div class="modal fade fixed top-0 left-0 w-full h-full outline-none overflow-x-hidden overflow-y-auto z-40 bg-black bg-opacity-70" tabindex="-1" @click="close">
    <div class="modal-dialog modal-dialog-scrollable relative w-auto pointer-events-none p-10" @click.stop="">
      <div
        class="modal-content border-none shadow-lg relative flex flex-col w-full pointer-events-auto bg-white bg-clip-padding rounded-md outline-none text-current">
        <div
          class="modal-header flex flex-shrink-0 items-center justify-between p-4 border-b border-gray-200 rounded-t-md">
          <h5 class="text-xl font-medium leading-normal text-gray-800">
            <slot name="title" />
          </h5>
          <button type="button" class="text-black text-3xl px-2" @click="close">
            <span aria-hidden="true">&times;</span>
            </button>
        </div>
        <div class="modal-body relative p-4">
          <slot name="body" />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: "Modal",
  methods: {
    close() {
      this.$emit("close");
    },
  },
};
</script>
