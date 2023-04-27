<script>
export default {
  name: "InfoTeam ",
  components: {},
};
</script>

<template>
    <div class="ms_team_info">
        <h1>Our Team<span class="text_primary">.</span></h1>
        <p class="py-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque et harum voluptatum suscipit exercitationem nobis quis eligendi aut. Dolore, veniam?</p>
        <div class="d-flex">
        <button class="btn rounded-0 bg_lighter d-flex align-items-center p-0 py-2 me-3">
            <div class="px-4 fw-bold">README</div>
            <div class="px-2 border-start border-dark border-1 text_dark fs-6">&#10230</div>
        </button>
        <button class="btn rounded-0 bg_primary text_lighter d-flex align-items-center p-0 py-2">
            <div class="px-4 ">PURCHASE</div>
            <div class="px-2 border-start  border-1 text_lighter fs-6">&#10230</div>
        </button>
        </div>
    </div>
    <!-- /.ms_team_info -->
</template>

<style lang="scss" scoped>
  .ms_team_info {
    position: absolute;
    top: 50%;
    width: 30%;
    transform: translate(0, -50%); //center H
    button{
      font-size: 0.8rem;
    }
}
</style>
