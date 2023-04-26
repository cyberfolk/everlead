<script>
export default {
  name: "PageFooter ",
  components: {},
};
</script>

<template>
  <footer>
    <section class="ms_footer_top bg_dark">
      <div class="container">
        <div class="row row-cols-4">
          <div class="col"><h5>About</h5></div>
          <!-- /.col -->
          <div class="col"><h5>Twitter</h5></div>
          <!-- /.col -->
          <div class="col"><h5>Important Links</h5></div>
          <!-- /.col -->
          <div class="col"><h5>Contact me</h5></div>
          <!-- /.col -->
        </div>
        <!-- /.row -->
      </div>
      <!-- /.container -->
    </section>
    <!-- /.ms_footer_top -->

    <section class="ms_footer_bottom bg_primary">
      <p class="text_light text-center">Copyright Everlead &#169;MikadoThemes</p>
    </section>
    <!-- /.ms_footer_bottom -->
  </footer>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;

h5 {
  color: $light;
}
</style>
