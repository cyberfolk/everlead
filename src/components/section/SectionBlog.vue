<script>
import ItemSlider from "../item/ItemSlider.vue";
export default {
  name: "SectionBlog",
  components: {
    ItemSlider,
  },
};
</script>

<template>
  <section>
    <div class="container">
      <h2>Latest news</h2>
      <ItemSlider />
    </div>
    <!-- /.container -->
  </section>
</template>
<style lang="scss" scoped></style>
