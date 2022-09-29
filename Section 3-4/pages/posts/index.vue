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
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          loadedPosts: [
            {
              id: "1",
              title: "First Post",
              previewText: "This is our first post!",
              thumbnail:
                "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fderf9v1xhwwx1.cloudfront.net%2Fimage%2Fupload%2Fc_fill%2Cq_60%2Ch_630%2Cw_1290%2Foth%2FFunimationStoreFront%2F1318871%2FJapanese%2F1318871_Japanese_KeyArt-OfficialVideoImage_06347d63-de55-e711-8175-020165574d09.jpg&f=1&nofb=1&ipt=509335ff4ca8472ffe3138d65b140f541ff3699f447b0f084742d5d04fff01f9&ipo=images",
            },
            {
              id: "2",
              title: "Second Post",
              previewText: "This is our second post!",
              thumbnail:
                "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fderf9v1xhwwx1.cloudfront.net%2Fimage%2Fupload%2Fc_fill%2Cq_60%2Ch_630%2Cw_1290%2Foth%2FFunimationStoreFront%2F1318871%2FJapanese%2F1318871_Japanese_KeyArt-OfficialVideoImage_06347d63-de55-e711-8175-020165574d09.jpg&f=1&nofb=1&ipt=509335ff4ca8472ffe3138d65b140f541ff3699f447b0f084742d5d04fff01f9&ipo=images",
            },
          ],
        });
      }, 1000);
      // reject(new Error());
    })
      .then((data) => {
        return data;
      })
      .catch((e) => {
        context.error(e);
      });
  },
  created() {
    this.$store.dispatch("setPosts", this.loadedPosts);
    console.log(this.$store.getters.loadedPosts);
  },
};
</script>

<style lang="scss" scoped></style>
