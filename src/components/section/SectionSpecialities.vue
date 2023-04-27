<script>
import specialities from "../../data/section/specialities.json";
export default {
  name: "SectionSpecialities",
  components: {},
  data() {
    return { specialities: specialities };
  },
};
</script>

<template>
  <section id="ms_specialities" class="bg_light">
    <div class="ms_big_container bg_lighter">
      <div class="ms_medium_container text-center">
        <h2 class="">Our specialities<span class="text_primary">.</span></h2>
        <p class="">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dignissimos, vitae.</p>
        <div class="spacer m-auto pb-5"></div>
        <div class="row row-cols-4">
          <div class="col" v-for="s in specialities">
            <img :src="s.path" alt="" />
            <h5 class="pt-4">{{ s.title }}</h5>
            <p>{{ s.text }}</p>
          </div>
          <!-- /.col -->
        </div>
        <!-- /.row -->
      </div>
      <!-- /.ms_medium_container -->
    </div>
    <!-- /.ms_big_container -->
  </section>
  <!-- /#ms_specialities -->
</template>

<style lang="scss" scoped>
.ms_big_container {
  padding: 5rem 0;
  position: relative;
  top: -50px; //to move it up like in the screenshot reference
}
</style>
