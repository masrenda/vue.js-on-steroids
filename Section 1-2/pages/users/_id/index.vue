<template>
  <div class="mx-auto container p-5 flex-col gap-5 text-center">
    <h1 class="font-extrabold text-4xl">Ini adalah halaman dinamis</h1>
    <p class="text-md">
      Rute URL sekarang adalah: http://localhost:3000/users/{{
        $route.params.id
      }}
    </p>
    <div class="pt-5">
      <button class="border px-1 border-slate-700">
        <nuxt-link to="/">Back to Home</nuxt-link>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  validate(data) {
    // return data.params.id == 1;
    return /^\d+$/.test(data.params.id);
  },
};
</script>

<style lang="scss" scoped></style>
