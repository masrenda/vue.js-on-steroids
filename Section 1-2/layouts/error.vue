<template>
  <div class="text-center p-5">
    <h1 class="text-md font-semibold">
      Mohon maaf, anda mengakses halaman yang mana?
    </h1>
    <p>soalnya kami tidak menyediakan halaman yang anda pinta</p>
    <div class="pt-5">
      <button class="border px-1 border-slate-700">
        <nuxt-link to="/">Back to Home</nuxt-link>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  layout: "users",
};
</script>

<style lang="scss" scoped></style>
