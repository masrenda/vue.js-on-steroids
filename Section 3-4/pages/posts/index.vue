<template>
  <div>
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script>
import PostList from "~/components/posts/PostList.vue";
export default {
  components: {
    PostList,
  },
  computed: {
    loadedPosts() {
      return this.$store.getters.loadedPosts;
    },
  },
  created() {
    this.$store.dispatch("setPosts", this.loadedPosts);
  },
};
</script>

<style lang="scss" scoped></style>
