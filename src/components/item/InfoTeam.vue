<script>
import ItemButton from "../item/ItemButton.vue";
export default {
  name: "InfoTeam ",
  components: { ItemButton },
};
</script>

<template>
  <div class="ms_team_info">
    <h1>Our Team<span class="text_primary">.</span></h1>
    <p class="py-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque et harum voluptatum suscipit exercitationem nobis quis eligendi aut. Dolore, veniam?</p>
    <div class="d-flex">
      <ItemButton :text="'READ MORE'" :color="'lighter'" />
      <ItemButton :text="'PURCHASE'" :color="'primary'" />
    </div>
  </div>
  <!-- /.ms_team_info -->
</template>

<style lang="scss" scoped>
.ms_team_info {
  position: absolute;
  left: 0;
  top: 50%;
  width: 40%;
  transform: translate(0, -50%); //center H
}
</style>
