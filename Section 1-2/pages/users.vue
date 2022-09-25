<template>
  <div>
    <Header />
    <div class="mx-auto container p-5 flex-col gap-5 text-center">
      <h1 class="font-extrabold text-4xl">
        Ini adalah halaman dalam folder users
      </h1>
      <p class="text-md">
        Rute URL sekarang adalah: http://localhost:3000/users
      </p>
      <div class="pt-4">
        <input type="text" class="border border-slate-700" v-model="iptWord" />
        <button class="border px-1 border-slate-700" @click="onLoadUser">
          Jalankan
        </button>
      </div>
      <nuxt />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      iptWord: "",
    };
  },
  methods: {
    onLoadUser() {
      this.$router.push("/users/" + this.iptWord);
    },
  },
  layout: "users",
};
</script>

<style lang="scss" scoped></style>
