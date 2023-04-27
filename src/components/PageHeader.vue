<script>
import ItemSlider from "./item/ItemSlider.vue";
import ItemNav from "./item/ItemNav.vue";
export default {
  name: "PageHeader ",
  components: {
    ItemSlider,
    ItemNav,
  },
};
</script>

<template>
  <header>
    <ItemNav />
    <div class="ms_big_container">
      <div class="ms_medium_container">
        <div><h1>Our Team.</h1></div>
        <ItemSlider />
      </div>
      <!-- /.ms_medium_container -->
    </div>
    <!-- /.ms_big_container -->
  </header>
</template>
<style lang="scss" scoped></style>
