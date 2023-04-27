<script>
import ItemSlider from "../item/ItemSlider.vue";
import ItemNews from "../item/ItemNews.vue";
export default {
  name: "SectionBlog",
  components: {
    ItemSlider,
    ItemNews,
  },
};
</script>

<template>
  <section id="ms_blog">
    <div class="ms_big_container">
      <div class="ms_medium_container">
        <div class="text-center">
          <h2>Latest news</h2>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing.</p>
          <div class="spacer m-auto pb-5"></div>
        </div>
        <div class="row row-cols-3 g-5">
          <div class="col">
            <ItemNews :path="'01.jpg'" :date="'May 6 2019'" :author="'Amanda Doe'" :title="'Next Investiment'" :text="'Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, veniam!'" />
          </div>
          <!-- /.col -->
          <div class="col">
            <ItemNews :path="'01.jpg'" :date="'May 6 2019'" :author="'Amanda Doe'" :title="'Next Investiment'" :text="'Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, veniam!'" />
          </div>
          <!-- /.col -->
          <div class="col">
            <ItemNews :path="'01.jpg'" :date="'May 6 2019'" :author="'Amanda Doe'" :title="'Next Investiment'" :text="'Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, veniam!'" />
          </div>
          <!-- /.col -->
        </div>
        <!-- /.row -->

        <!-- /.spacer -->
        <ItemSlider />
      </div>
      <!-- /.ms_medium_container -->
      <img class="dot" src="../../assets/img/icon/o-dot.svg" alt="" />
    </div>
    <!-- /.ms_big_container -->
  </section>
  <!-- /#ms_blog -->
</template>
<style lang="scss" scoped>
@use "../../assets/scss/partials/variables" as *;
#ms_blog {
  background-color: $light;
  padding: 8rem 0;
  .ms_big_container {
    position: relative;
    .row {
      position: relative;
      z-index: 1;
    }
    .dot {
      position: absolute;
      top: -40%;
      left: 0;
      z-index: 0;
    }
  }
}
</style>
