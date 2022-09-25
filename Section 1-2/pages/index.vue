<template>
  <div>
    <Header />
    <div class="mx-auto justify-center text-center p-5">
      <h1 class="font-extrabold text-4xl">Ini adalah halaman Root (/)</h1>
      <div class="pt-5">
        <button class="border px-1 border-slate-700">
          <nuxt-link to="/users">Open The Gate</nuxt-link>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NuxtTutorial",
  layout: "users",
};
</script>
