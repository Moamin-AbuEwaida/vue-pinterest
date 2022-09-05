<template>
  <div @mouseover="hover = true" @mouseleave="hover = false" class="relative">
    <img :src="src" alt="" class="rounded-lg" />
    <div
      v-if="hover"
      class="absolute bg-dark opacity-50 inset-0 w-full h-full rounded-lg"
    ></div>
    <div
      v-if="hover"
      class="absolute top-0 w-full h-full flex flex-col justify-between p-3"
    >
      <div class="flex items-center justify-between">
        <button class="flex items-center">
          <p class="font-semibold text-white">{{ board }}</p>
          <span class="material-icons text-white">expand_more</span>
        </button>
        <button
          class="rounded-full px-5 py-3 text-white bg-primary font-semibold"
        >
          Save
        </button>
      </div>
      <div class="flex items-center w-full">
        <button
          class="ml-auto bg-white rounded-full w-8 h-8 mr-2 text-dark opacity-75 hover:opacity-100 flex items-center justify-center"
        >
          <span class="material-icons text-base">ios_share</span>
        </button>
        <button
          class="bg-white rounded-full w-8 h-8 text-dark opacity-75 hover:opacity-100 flex items-center justify-center"
        >
          <span class="material-icons text-base">more_horiz</span>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["src", "board"],
  data() {
    return {
      hover: false,
    };
  },
};
</script>

<style></style>
