<template>
  <div class="container mx-auto p-5">
    <section class="text-center">
      <AppButton
        @click="$router.push('/admin/new-post')"
        class="border border-slate-500 px-1"
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
  components: {
    PostList,
    AppButton,
  },
};
</script>

<style lang="scss" scoped></style>
