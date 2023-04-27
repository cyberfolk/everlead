<script>
export default {
  name: "SectionPhoto",
  components: {},
};
</script>

<template>
  <section id="ms_photo">
    <img class="w-100" src="../../assets/img/section/photo/03.jpg" alt="" />
    <i class="play fa-solid fa-play text_light fa-5x"></i>
  </section>
  <!-- /#ms_photo -->
</template>
<style lang="scss" scoped>
#ms_photo {
  position: relative;
  .play {
    position: absolute;
    left: 50%;
    top: 50%;
  }
}
</style>
