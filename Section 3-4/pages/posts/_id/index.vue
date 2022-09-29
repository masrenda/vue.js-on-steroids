<template>
  <div>
    <div class="container p-5 mx-auto">
      <section class="flex flex-col gap-5 text-center divide-y">
        <div>
          <div class="text-2xl">{{ loadedPost.title }}</div>
          <div class="text-2xl">{{ loadedPost.author }}</div>
          <div class="text-2xl">{{ loadedPost.updateDate }}</div>
          <div class="text-2xl">{{ loadedPost.content }}</div>
        </div>
        <div>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat
            quos fuga quaerat doloremque possimus. Autem ab reiciendis vel
            temporibus aspernatur quas eligendi tempora vitae, cum neque libero
            quibusdam voluptates id beatae. Qui rerum dolor architecto. Nisi in
            voluptatem accusamus dolores?
          </p>
          <p>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Explicabo
            doloremque incidunt repellat aperiam ipsam non, voluptate placeat
            aliquid reiciendis libero a maiores eveniet numquam praesentium nam
            culpa necessitatibus distinctio, ea nihil, esse error quod omnis.
            Quod vitae similique molestias! Magnam id dignissimos odio sequi
            assumenda iste quibusdam, nihil atque, adipisci veniam quaerat,
            sapiente deleniti reiciendis totam. Ad ab nostrum sit voluptatem
            odit eveniet similique quis maiores tempora vero. Molestiae
            voluptatibus quisquam eum iusto dignissimos eius repellendus
            repudiandae. Hic, nihil modi.
          </p>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  asyncData(context, callback) {
    setTimeout(() => {
      callback(null, {
        loadedPost: {
          id: "",
          title: "First Post (ID: " + context.route.params.id + " )",
          author: "Taren",
          updateDate: new Date(),
          content: "Some dummy text here",
          thumbnail:
            "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fderf9v1xhwwx1.cloudfront.net%2Fimage%2Fupload%2Fc_fill%2Cq_60%2Ch_630%2Cw_1290%2Foth%2FFunimationStoreFront%2F1318871%2FJapanese%2F1318871_Japanese_KeyArt-OfficialVideoImage_06347d63-de55-e711-8175-020165574d09.jpg&f=1&nofb=1&ipt=509335ff4ca8472ffe3138d65b140f541ff3699f447b0f084742d5d04fff01f9&ipo=images",
        },
      });
    }, 1000);
  },
};
</script>

<style lang="scss" scoped></style>
