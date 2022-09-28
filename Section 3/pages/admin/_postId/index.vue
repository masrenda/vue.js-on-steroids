<template>
  <div class="mx-auto container">
    <AdminPostForm :post="loadedPost" />
  </div>
</template>

<script>
import AdminPostForm from "~/components/Admin/AdminPostForm.vue";
export default {
  layout: "admin",
  components: { AdminPostForm },
  data() {
    return {
      loadedPost: {
        author: "Tarenadiyaksa",
        title: "My Awesome Post",
        content: "Super Amazing Lmao",
        thumbnailLink: "https://a.ppy.sh/22435935?1645473442.jpeg",
      },
    };
  },
};
</script>

<style lang="scss" scoped></style>
