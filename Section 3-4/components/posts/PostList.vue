<template>
  <div>
    <div class="container p-5 mx-auto">
      <div class="bg-[url('~/assets/images/51130.jpg')]">
        <h1 class="text-2xl text-center">RIENCARNATION'S BLOG</h1>
        <div class="flex flex-col gap-4 divide-y-2">
          <PostPreview
            v-for="post in posts"
            :key="post.id"
            :id="post.id"
            :is-admin="isAdmin"
            :thumbnail="post.thumbnail"
            :title="post.title"
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
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss" scoped></style>
