<script>
import photoHeader from "../data/photo-Header.json";
import ItemNav from "./item/ItemNav.vue";
import InfoTeam from "./item/InfoTeam.vue";
export default {
  name: "PageHeader ",
  components: {
    ItemNav,
    InfoTeam,
  },
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
  <header class="bg_light">
    <ItemNav />
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
  </header>
</template>

<style lang="scss" scoped>
header {
  height: 900px;
  position: relative;
  img {
    object-fit: cover;
  }
}
</style>
