<script>
import ItemSlider from "../item/ItemSlider.vue";
export default {
  name: "SectionTestimonials",
  components: {
    ItemSlider,
  },
};
</script>

<template>
  <section id="ms_testimonials" class="bg_darkless">
    <div class="bg_text text_dark">Testimonials.</div>
    <!-- /.bg_text -->
  </section>
  <!-- /.ms_testimonials -->
</template>

<style lang="scss" scoped>
section {
  position: relative;
  .bg_text {
    text-align: center;
    font-size: 200px !important;
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    overflow: hidden;
    line-height: 0.9;
    font-family: "Libre Baskerville", serif;
  }
}
</style>
