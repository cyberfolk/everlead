<script>
export default {
  name: "SectionContact",
  components: {},
};
</script>

<template>
  <section id="ms_contact" class="bg_light">
    <div class="ms_big_container">
      <div class="ms_medium_container">
        <div class="row row-cols-2">
          <div class="col">
            <div class="ms_map_container">
              <img class="ms_map" src="../../assets/img/section/contact/map.png" alt="" />
              <img class="ms_plus ms_1" src="../../assets/img/section/contact/plus.png" alt="" />
              <img class="ms_plus ms_2" src="../../assets/img/section/contact/plus.png" alt="" />
              <img class="ms_plus ms_3" src="../../assets/img/section/contact/plus.png" alt="" />
            </div>
          </div>
          <!-- /.col -->
          <div class="col"><h2>Contact us</h2></div>
          <!-- /.col -->
        </div>
        <!-- /.row -->
      </div>
      <!-- /.ms_medium_container -->
    </div>
    <!-- /.ms_big_container -->
  </section>
  <!-- /#ms_contact -->
</template>
<style lang="scss" scoped>
.ms_map_container {
  position: relative;
  .ms_plus {
    position: absolute;
    display: block;
  }
  .ms_1 {
    top: 35%;
    left: 24%;
  }
  .ms_2 {
    top: 22.5%;
    left: 52.5%;
  }
  .ms_3 {
    top: 72.5%;
    left: 85%;
  }
}
</style>
