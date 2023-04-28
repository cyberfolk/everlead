<script>
import testimonials from "../../data/section/testimonials.json";
import ItemSlider from "../item/ItemSlider.vue";
export default {
  name: "SectionTestimonials",
  components: { ItemSlider },
  data() {
    return {
      activeImage: 0,
      percentage: 33,
      testimonials: testimonials,
    };
  },
  methods: {
    next() {
      this.activeImage++;
      if (this.activeImage == this.testimonials.length) {
        this.activeImage = 0;
      }
      this.calcPercentage();
    },
    prev() {
      this.activeImage--;
      if (this.activeImage < 0) {
        this.activeImage = this.testimonials.length - 1;
      }
      this.calcPercentage();
    },
    calcPercentage() {
      this.percentage = Math.ceil((100 * (this.activeImage + 1)) / this.testimonials.length);
    },
  },
};
</script>

<template>
  <section id="ms_testimonials" class="bg_darkless">
    <div class="bg_text text_dark position-absolute top-0 start-50 translate-middle-x">Testimonials.</div>
    <!-- /.bg_text -->
    <div class="ms_big_container">
      <button class="ms_arrow bg-transparent text_light border-0 start-0" @click="prev()">&LongLeftArrow;</button>
      <button class="ms_arrow bg-transparent text_light border-0 end-0" @click="next()">&LongRightArrow;</button>
      <div class="ms_medium_container">
        <div class="m-auto text-center">
          <img class="border border-3 rounded-circle border-white m-3" :src="testimonials[activeImage].path" alt="" />
          <h5 class="text_light m-4">{{ testimonials[activeImage].name }}</h5>
          <p class="w-50 m-auto text-center pb-4">{{ testimonials[activeImage].text }}</p>

          <div class="d-flex align-items-center justify-content-center">
            <div class="text_light">{{ "0" + (activeImage + 1) }}</div>
            <div class="bar m-2">
              <div :style="{ width: percentage + '%' }" class="bar up m-0"></div>
            </div>
            <div class="text_light">{{ "0" + testimonials.length }}</div>
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
  .bg_text {
    font-size: 200px;
    line-height: 1;
    font-family: "Libre Baskerville", serif;
  }
  .ms_big_container {
    position: relative;
    padding: 8rem 0;
    z-index: 1;
  }
  .bar {
    height: 0.1rem;
    background-color: $secondary;
    width: 10%;
  }
  .bar.up {
    background-color: $light;
  }
}
</style>
