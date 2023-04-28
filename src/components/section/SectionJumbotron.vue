<script>
import photoHeader from "../../data/photo-Header.json";
import InfoTeam from "../item/InfoTeam.vue";
export default {
  name: "PageHeader ",
  components: { InfoTeam },
  data() {
    return {
      activeImage: 0,
      photos: photoHeader,
    };
  },
  methods: {
    next() {
      this.activeImage++;
      if (this.activeImage == this.photos.length) {
        this.activeImage = 0;
      }
    },
    prev() {
      this.activeImage--;
      if (this.activeImage < 0) {
        this.activeImage = this.photos.length - 1;
      }
    },
  },
};
</script>

<template>
  <section id="ms_jumbotron">
    <img class="h-100 w-100" :src="photos[activeImage].path" alt="" />
    <div class="ms_big_container h_centering">
      <button class="ms_arrow bg-transparent border-0 start-0" @click="prev()">&LongLeftArrow;</button>
      <button class="ms_arrow bg-transparent border-0 end-0" @click="next()">&LongRightArrow;</button>
      <div class="ms_medium_container h_centering">
        <InfoTeam />
      </div>
      <!-- /.ms_medium_container -->
    </div>
    <!-- /.ms_big_container -->
  </section>
  <!-- /#ms_jumbotron -->
</template>

<style lang="scss" scoped>
#ms_jumbotron {
  height: 900px;
  position: relative;
  img {
    object-fit: cover;
  }
}
</style>
