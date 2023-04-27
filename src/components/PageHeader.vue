<script>
import ItemSlider from "./item/ItemSlider.vue";
import ItemNav from "./item/ItemNav.vue";
import InfoTeam from "./item/InfoTeam.vue";
export default {
  name: "PageHeader ",
  components: {
    ItemSlider,
    ItemNav,
    InfoTeam,
  },
};
</script>

<template>
  <header class="bg_light">
    <ItemNav />
    <div class="ms_big_container">
      <div class="ms_medium_container">
        <InfoTeam />
        <ItemSlider />
      </div>
      <!-- /.ms_medium_container -->
    </div>
    <!-- /.ms_big_container -->
  </header>
</template>

<style lang="scss" scoped>
header {
  height: 500px;
  position: relative;
}
</style>
