<script>
export default {
  name: "CardEvent",
  components: {},
  props: {
    title: String,
    date: String,
    location: String,
  },
};
</script>

<template>
  <div class="ms_card_event d-flex px-5 py-4 border-bottom">
    <div class="ms_card_date_cell pe-3">
      <div class="square p-2 text-center bg_primary text_lighter">
        <div class="ms_card_date_day"><h6 class="mb-0">22</h6></div>
        <div class="ms_card_date_month_year text_light fs_08">Jan, 2022</div>
      </div>
      <!-- /.square -->
    </div>
    <!-- /.ms_card_date_cell -->
    <div class="ms_card_info_cell">
      <div class="ms_card_info_name">
        <h6>{{ title }}</h6>
      </div>
      <ul class="fa-ul ms-4">
        <li class="fs_08">
          <span class="fa-li"><i class="fa-regular fa-clock text_primary"></i></span>
          <p class="mb-1">{{ date }}</p>
        </li>
        <li class="fs_08">
          <span class="fa-li"><i class="fa-solid fa-location-dot text_primary"></i></span>
          <p>{{ location }}</p>
        </li>
      </ul>
      <div class="fw-bold fs_08">READ MORE</div>
    </div>
    <!-- /.ms_card_info_cell -->
  </div>
  <!-- /.ms_card_event -->
</template>

<style lang="scss" scoped></style>
