<script>
export default {
  name: "SectionBlog",
  components: {},
  props: {
    path: String,
    date: String,
    author: String,
    title: String,
    text: String,
  },
};
</script>

<template>
  <div class="ms_news">
    <img class="w-100 pb-4" :src="path" alt="" />
    <div class="fs_08 pb-2">
      <i class="text_primary fa-regular fa-clock pe-1"></i>
      <span class="pe-2">{{ date }}</span>
      <i class="text_primary fa-solid fa-user pe-1"></i>
      <span>{{ author }}</span>
    </div>
    <h5>{{ title }}</h5>
    <p>{{ text }}</p>
    <div class="fs_08 fw-bold">READ MORE</div>
  </div>
  <!-- /.ms_news -->
</template>
<style lang="scss" scoped>
@use "../../assets/scss/partials/variables" as *;
</style>
