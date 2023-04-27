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
  <section id="ms_blog">
    <div class="ms_big_container">
      <div class="ms_medium_container">
        <h2>Latest news</h2>
        <ItemSlider />
      </div>
      <!-- /.ms_medium_container -->
    </div>
    <!-- /.ms_big_container -->
  </section>
  <!-- /#ms_blog -->
</template>
<style lang="scss" scoped></style>
