<template>
  <div class="container mx-auto">
    <AdminPostForm />
  </div>
</template>

<script>
import AdminPostForm from "~/components/Admin/AdminPostForm.vue";
export default {
  layout: "admin",
  components: {
    AdminPostForm,
  },
};
</script>

<style lang="scss" scoped></style>
