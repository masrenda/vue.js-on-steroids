<template>
  <div class="text-center">
    <div>Get Your Posts Here:</div>
    <div
      class="w-40 h-40 mx-auto bg-cover"
      :style="{ backgroundImage: `url(${thumbnail})` }"
    ></div>
    <button class="border mt-2 border-slate-500 px-1">
      <nuxt-link :to="postLink">{{ title }}</nuxt-link>
    </button>
  </div>
</template>

<script>
export default {
  name: "PostPreview",
  props: {
    id: {
      type: String,
      required: true,
    },
    isAdmin: {
      type: Boolean,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    thumbnail: {
      type: String,
      required: true,
    },
  },
  computed: {
    postLink() {
      return this.isAdmin ? "/admin/" + this.id : "/posts/" + this.id;
    },
  },
};
</script>

<style lang="scss" scoped></style>
