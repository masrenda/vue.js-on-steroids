<template>
  <div>
    <div class="mx-auto container p-5">
      <div class="bg-[url('~/assets/images/51130.jpg')]">
        <h1 class="text-center text-2xl">RIENCARNATION'S BLOG</h1>
        <div class="divide-y-2 flex flex-col gap-4">
          <PostPreview
            id="1"
            :is-admin="isAdmin"
            thumbnail="https://a.ppy.sh/22435935?1645473442.jpeg"
            title="Post 1"
          />
          <PostPreview
            id="2"
            :is-admin="isAdmin"
            thumbnail="https://a.ppy.sh/22435935?1645473442.jpeg"
            title="Post 2"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import PostPreview from "~/components/posts/PostPreview.vue";
export default {
  components: {
    PostPreview,
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="scss" scoped></style>
