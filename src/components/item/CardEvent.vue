<script>
export default {
  name: "CardEvent",
  props: {
    title: String,
    duration: String,
    date: String,
    location: String,
  },
  data() {
    return { luxonDate: null };
  },
  created() {
    this.luxonDate = luxon.DateTime.fromFormat(this.date, "MMM dd, yyyy");
  },
};
</script>

<template>
  <div class="ms_card_event d-flex px-5 py-4 border-bottom bg_light">
    <div class="ms_card_cell pe-3">
      <div class="square p-2 text-center bg_primary text_lighter">
        <h6 class="mb-0">{{ luxonDate.toFormat("dd") }}</h6>
        <div class="text_light fs_08">{{ luxonDate.toFormat("MMM, yyyy") }}</div>
      </div>
      <!-- /.square -->
    </div>
    <!-- /.ms_card_cell -->
    <div class="ms_card_cell">
      <h5>{{ title }}</h5>
      <ul class="fa-ul ms-4">
        <li class="fs_08">
          <span class="fa-li"><i class="fa-regular fa-clock text_primary"></i></span>
          <p class="mb-1">{{ duration + ", " + date }}</p>
        </li>
        <li class="fs_08">
          <span class="fa-li"><i class="fa-solid fa-location-dot text_primary"></i></span>
          <p>{{ location }}</p>
        </li>
      </ul>
      <div class="fw-bold fs_08">READ MORE</div>
    </div>
    <!-- /.ms_card_cell -->
  </div>
  <!-- /.ms_card_event -->
</template>

<style lang="scss" scoped>
@use "../../assets/scss/partials/variables" as *;
.ms_card_event:hover {
  background-color: $lighter;
  h5 {
    color: $primary;
  }
}
</style>
