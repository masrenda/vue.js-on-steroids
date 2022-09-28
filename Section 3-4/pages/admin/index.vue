<template>
  <div class="container p-5 mx-auto">
    <section class="text-center">
      <AppButton
        @click="$router.push('/admin/new-post')"
        class="px-1 border border-slate-500"
      >
        Create a posts
      </AppButton>
    </section>
    <section>
      <PostList isAdmin />
    </section>
  </div>
</template>

<script>
import PostList from "~/components/posts/PostList.vue";
import AppButton from "~/components/UI/AppButton.vue";

export default {
  layout: "admin",
  components: {
    PostList,
    AppButton,
  },
};
</script>

<style lang="scss" scoped></style>
