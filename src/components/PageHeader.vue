<script>
import ItemNav from "./item/ItemNav.vue";
import InfoTeam from "./item/InfoTeam.vue";
export default {
  name: "PageHeader ",
  components: {
    ItemNav,
    InfoTeam,
  },
};
</script>

<template>
  <header class="bg_light">
    <img class="h-100 w-100" src="../assets/img/header/02.jpg" alt="" />
    <ItemNav />
    <div class="ms_big_container">
      <div class="ms_medium_container">
        <InfoTeam />
      </div>
      <!-- /.ms_medium_container -->
    </div>
    <!-- /.ms_big_container -->
  </header>
</template>

<style lang="scss" scoped>
header {
  height: 900px;
  position: relative;
  img {
    object-fit: cover;
  }
}
</style>
