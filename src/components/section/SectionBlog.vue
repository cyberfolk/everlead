<script>
import blog from "../../data/section/blog.json";
import ItemSlider from "../item/ItemSlider.vue";
import ItemNews from "../item/ItemNews.vue";
export default {
  name: "SectionBlog",
  components: {
    ItemSlider,
    ItemNews,
  },
  data() {
    return { blog: blog };
  },
};
</script>

<template>
  <section id="ms_blog" class="bg_light">
    <div class="ms_big_container">
      <div class="ms_medium_container">
        <div class="text-center">
          <h2>Latest news<span class="text_primary">.</span></h2>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing.</p>
          <div class="spacer m-auto pb-5"></div>
        </div>
        <div class="row row-cols-3 g-5">
          <div v-for="news in blog.slice(0, 3)" class="col">
            <ItemNews :path="news.path" :date="news.date" :author="news.author" :title="news.title" :text="news.text" />
          </div>
          <!-- /.col -->
        </div>
        <!-- /.row -->
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
