<template>
  <div class="px-3 py-4 flex items-center justify-between">
    <div class="flex items-center">
      <button
        class="rounded-full hover:bg-light p-3 flex items-center justify-center"
        type="button"
        name="button"
      >
        <img src="logoP.png" alt="logo" class="h-6 w-6" />
      </button>
      <button
        v-for="(item, i) in tabItems"
        :key="i"
        @click="selectedTab = item.key"
        :class="`${
          selectedTab === item.key
            ? 'bg-dark text-white'
            : 'text-dark hover:bg-light'
        } rounded-full py-3 px-4 font-semibold`"
        type="button"
        name="button"
      >
        {{ item.name }}
      </button>
    </div>
    <div class="flex flex-grow relative">
      <span class="material-icons absolute mt-3 ml-3 text-muted"> search </span>
      <input
        class="text-muted w-full rounded-full bg-light py-3 pr-3 pl-10 hover:bg-lightHover"
        type="text"
        name=""
        value=""
        placeholder="Search"
      />
    </div>
    <div class="flex items-center">
      <button
        class="relative rounded-full hover:bg-light flex items-center justify-center p-3"
      >
        <span class="material-icons text-3xl text-muted">notifications</span>
        <div
          class="absolute rounded-full w-5 h-5 bg-primary text-white flex items-center justify-center mb-5 ml-5"
        >
          1
        </div>
      </button>
      <button
        class="relative rounded-full hover:bg-light flex items-center justify-center p-3"
      >
        <span class="material-icons text-3xl text-muted">textsms</span>
        <div
          class="absolute rounded-full w-5 h-5 bg-primary text-white flex items-center justify-center mb-5 ml-5"
        >
          3
        </div>
      </button>
      <button
        class="rounded-full hover:bg-light p-3 flex items-center justify-center"
        type="button"
        name="button"
      >
        <div
          class="w-6 h-6 bg-cover bg-center rounded-full"
          style="background-image: url(profile.jpg)"
        ></div>
      </button>
      <button
        class="w-6 h-6 hover:bg-light rounded-full flex items-center justify-center"
      >
        <span class="material-icons text-muted">expand_more</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tabItems: [
        { name: "Home", key: "home" },
        { name: "Today", key: "today" },
      ],
      selectedTab: "home",
    };
  },
};
</script>

<style></style>
