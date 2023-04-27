<script>
import testimonials from "../../data/section/testimonials.json";
import ItemSlider from "../item/ItemSlider.vue";
export default {
  name: "SectionTestimonials",
  components: { ItemSlider },
  data() {
    return {
      percentage: 33,
      testimonials: testimonials,
    };
  },
};
</script>

<template>
  <section id="ms_testimonials" class="bg_darkless">
    <div class="bg_text text_dark"></div>
    <!-- /.bg_text -->
    <div class="ms_big_container">
      <div class="ms_medium_container">
        <div class="m-auto text-center">
          <img class="border border-3 rounded-circle border-white m-3" :src="testimonials[0].path" alt="" />
          <h5 class="text_light m-4">{{ testimonials[0].name }}</h5>
          <p class="w-50 m-auto text-center pb-4">{{ testimonials[0].text }}</p>
          <div class="d-flex align-items-center justify-content-center">
            <div class="text_light">01</div>
            <div class="bar">
              <div :style="{ width: percentage + '%' }" class="bar up"></div>
            </div>
            <div class="text_light">03</div>
          </div>
        </div>
      </div>
      <!-- /.ms_medium_container -->
    </div>
    <!-- /.ms_big_container -->
  </section>
  <!-- #.ms_testimonials -->
</template>

<style lang="scss" scoped>
@use "../../assets/scss/partials/variables" as *;

section {
  position: relative;
  .bg_text::after {
    content: "Testimonials.";
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
  .ms_big_container {
    position: relative;
    padding: 8rem 0;
    z-index: 1;
  }
  .bar {
    border-radius: 0.5rem;
    height: 0.1rem;
    position: relative;
    background-color: $secondary;
    z-index: 0;
    margin: 0 0.5rem;
    width: 10%;
  }
  .bar.up {
    cursor: pointer;
    top: 0;
    left: 0;
    position: absolute;
    background-color: $light;
    margin: 0rem;
    z-index: 1;
    width: 33%;
  }
}
</style>
