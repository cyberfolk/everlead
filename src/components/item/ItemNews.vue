<script>
export default {
  name: "SectionBlog",
  components: {},
  props: {
    news: Object,
  },
};
</script>

<template>
  <div class="col">
    <div class="ms_news" v-if="news">
      <img class="w-100 pb-4" :src="news.path" alt="" />
      <div class="fs_08 pb-2">
        <i class="text_primary fa-regular fa-clock pe-1"></i>
        <span class="pe-2">{{ news.date }}</span>
        <i class="text_primary fa-solid fa-user pe-1"></i>
        <span>{{ news.author }}</span>
      </div>
      <h5>{{ news.title }}</h5>
      <p>{{ news.text }}</p>
      <div class="fs_08 fw-bold">READ MORE</div>
    </div>
    <!-- /.ms_news -->
  </div>
  <!-- /.col -->
</template>
<style lang="scss" scoped>
@use "../../assets/scss/partials/variables" as *;

img {
  height: 270px;
  object-fit: cover;
}
</style>
