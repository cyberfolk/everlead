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
    <div class="container">
      <div><h1>Our Team.</h1></div>
      <ItemSlider />
    </div>
    <!-- /.container -->
  </header>
</template>
<style lang="scss" scoped></style>
