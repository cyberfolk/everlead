<script>
import events from "../../data/section/events.json";
import CardEvent from "../item/CardEvent.vue";
export default {
  name: "SectionEvents",
  components: { CardEvent },
  data() {
    return { events: events };
  },
};
</script>

<template>
  <section id="ms_events">
    <div class="ms_big_container">
      <div class="ms_medium_container">
        <div class="ms_card bg_lighter">
          <div class="ms_card_title shadow-sm px-5 py-4"><h4>Upcoming Events</h4></div>
          <CardEvent v-for="e in events" :title="e.title" :duration="e.duration" :date="e.date" :location="e.location" />
        </div>
        <!-- /.ms_card -->
      </div>
      <!-- /.ms_medium_container -->
    </div>
    <!-- /.ms_big_container -->
  </section>
  <!-- /#ms_events -->
</template>

<style lang="scss" scoped>
@use "../../assets/scss/partials/variables" as *;

section {
  background-image: url("../../assets/img/section/events/bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  .ms_medium_container {
    padding: 8rem 0;
    .ms_card {
      width: 40%;
    }
  }
}
</style>
