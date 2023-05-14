<script>
import blog from "../../data/section/blog.json";
import ItemNews from "../item/ItemNews.vue";
export default {
  name: "SectionBlog",
  components: {
    ItemNews,
  },
  data() {
    return {
      activeNews: 0,
      blog: blog,
    };
  },
  methods: {
    next() {
      this.activeNews += 3;
      if (this.activeNews > this.blog.length) {
        this.activeNews = 0;
      }
    },
    prev() {
      this.activeNews -= 3;
      if (this.activeNews < 0) {
        this.activeNews = Math.floor(this.blog.length / 3) * 3;
      }
    },
  },
};
</script>

<template>
  <section id="ms_blog" class="bg_light">
    <div class="ms_big_container">
      <button class="ms_arrow bg-transparent border-0 start-0" @click="prev()">&LongLeftArrow;</button>
      <button class="ms_arrow bg-transparent border-0 end-0" @click="next()">&LongRightArrow;</button>
      <div class="ms_medium_container">
        <div class="text-center">
          <h2>Latest news<span class="text_primary">.</span></h2>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing.</p>
          <div class="spacer m-auto pb-5"></div>
        </div>
        <div class="row row-cols-3 g-5">
          <ItemNews :news="blog[activeNews]" />
          <ItemNews :news="blog[activeNews + 1]" />
          <ItemNews :news="blog[activeNews + 2]" />
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
}</style>
