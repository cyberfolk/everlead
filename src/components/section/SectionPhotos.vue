<script>
import photos from "../../data/section/photos.json";
export default {
  name: "SectionPhoto",
  components: {},
  data() {
    return {
      autoPlay: null,
      activeImage: 0,
      photos: photos,
    };
  },
  methods: {
    next() {
      this.activeImage++;
      if (this.activeImage == this.photos.length) {
        this.activeImage = 0;
      }
    },
    play() {
      this.autoPlay = setInterval(this.next, 3000);
    },
    stop() {
      this.autoPlay = clearInterval(this.autoPlay);
    },
  },
};
</script>

<template>
  <section id="ms_photo">
    <img class="h-100 w-100" :src="photos[activeImage].path" alt="" />
    <button @click="autoPlay ? stop() : play()">
      <i class="hv_centering fa-solid fa-play text_light fa-5x"></i>
    </button>
  </section>
  <!-- /#ms_photo -->
</template>

<style lang="scss" scoped>
#ms_photo {
  position: relative;
  height: 1000px;
  img {
    object-fit: cover;
  }
}
</style>
