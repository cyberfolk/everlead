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
      <h5>{{ name }}</h5>
      <h5>{{ percentage }}%</h5>
    </div>
    <div class="bar">
      <div :style="{ width: percentage + '%' }" class="bar up"></div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
