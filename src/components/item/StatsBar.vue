<script>
export default {
  name: "StatsBar",
  components: {},
  props: {
    name: String,
    percentage: Number,
  },
};
</script>

<template>
  <div class="ms_stat pb-4">
    <div class="d-flex justify-content-between">
      <h6>{{ name }}</h6>
      <h6>{{ percentage }}%</h6>
    </div>
    <div class="bar">
      <div :style="{ width: percentage + '%' }" class="bar up"></div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../../assets/scss/partials/variables" as *;
.bar {
  border-radius: 0.5rem;
  height: 0.3rem;
  position: relative;
  background-color: $lightless;
  z-index: 0;
}
.bar.up {
  cursor: pointer;
  top: 0;
  left: 0;
  position: absolute;
  background-color: $primary;
  z-index: 1;
}
</style>
