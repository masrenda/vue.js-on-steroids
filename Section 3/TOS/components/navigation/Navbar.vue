<template>
  <div class="top-0 sticky z-10 w-full bg-zinc-900">
    <div class="flex flex-wrap justify-between">
      <div class="p-5 text-white font-cff">Logo</div>
      <div class="p-5 text-white">
        <button
          @click="isOpen = !isOpen"
          class="flex flex-col gap-2 scale-75 md:hidden"
        >
          <span class="block h-0.5 w-8 animate-pulse bg-gray-100"></span>
          <span class="block h-0.5 w-8 animate-pulse bg-gray-100"></span>
          <span class="block h-0.5 w-8 animate-pulse bg-gray-100"></span>
        </button>
      </div>
    </div>
    <div
      :class="isOpen ? 'block' : 'hidden'"
      class="flex flex-col items-center gap-8 p-5 text-white font-cff md:px-5 md:flex-row md:inline-flex md:absolute md:top-0 md:right-0"
    >
      <nuxt-link class="text-red-600" to="/admin">Admin</nuxt-link>
      <nuxt-link to="/">Home</nuxt-link>
      <nuxt-link to="/about">About</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
    };
  },
};
</script>
