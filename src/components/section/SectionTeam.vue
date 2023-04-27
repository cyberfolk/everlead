<script>
import ItemSlider from "../item/ItemSlider.vue";
export default {
  name: "SectionTeam",
  components: {
    ItemSlider,
  },
};
</script>

<template>
  <section id="ms_team" class="bg_light">
    <div class="ms_big_container">
      <div class="ms_medium_container">
        <ItemSlider class="slider_tmp" />
        <div class="ms_info_member bg_lighter">
          <h2>Nome team member</h2>
          <p>Role team member</p>
          <div class="spacer pt-3"></div>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum rem vero accusamus provident, repellendus veritatis consequuntur eius soluta alias aut?</p>
          <span>
            <svg id="icon_facebook" width="30px" viewBox="0 0 67 67"><path d="M29.765,50.32h6.744V33.998h4.499l0.596-5.624h-5.095  l0.007-2.816c0-1.466,0.14-2.253,2.244-2.253h2.812V17.68h-4.5c-5.405,0-7.307,2.729-7.307,7.317v3.377h-3.369v5.625h3.369V50.32z   M34,64C17.432,64,4,50.568,4,34C4,17.431,17.432,4,34,4s30,13.431,30,30C64,50.568,50.568,64,34,64z" /></svg>
            <svg id="icon_linkedin" width="30px" viewBox="0 0 67 67"><path d="M50.837,48.137V36.425c0-6.275-3.35-9.195-7.816-9.195  c-3.604,0-5.219,1.983-6.119,3.374V27.71h-6.79c0.09,1.917,0,20.427,0,20.427h6.79V36.729c0-0.609,0.044-1.219,0.224-1.655  c0.49-1.22,1.607-2.483,3.482-2.483c2.458,0,3.44,1.873,3.44,4.618v10.929H50.837z M22.959,24.922c2.367,0,3.842-1.57,3.842-3.531  c-0.044-2.003-1.475-3.528-3.797-3.528s-3.841,1.524-3.841,3.528c0,1.961,1.474,3.531,3.753,3.531H22.959z M34,64  C17.432,64,4,50.568,4,34C4,17.431,17.432,4,34,4s30,13.431,30,30C64,50.568,50.568,64,34,64z M26.354,48.137V27.71h-6.789v20.427  H26.354z" /></svg>
            <svg id="icon_twitter" width="30px" viewBox="0 0 30 30"><path d="M22.1,10.2c-0.5,0.3-1.1,0.4-1.7,0.5c0.6-0.4,1.1-1,1.3-1.7c-0.6,0.3-1.2,0.6-1.9,0.8c-0.6-0.6-1.3-1-2.1-1	c-1.6,0-3,1.4-3,3.2c0,0.2,0,0.5,0.1,0.7c-2.5-0.1-4.7-1.4-6.1-3.3c-0.3,0.4-0.4,1-0.4,1.6c0,1.1,0.5,2.1,1.3,2.6	c-0.5,0-1-0.2-1.3-0.4v0.1c0,1.5,1,2.8,2.4,3.1c-0.2,0.1-0.5,0.1-0.8,0.1c-0.2,0-0.4,0-0.6-0.1c0.4,1.3,1.5,2.2,2.8,2.2	c-1,0.8-2.3,1.3-3.7,1.3c-0.2,0-0.4,0-0.7-0.1c1.3,0.9,2.9,1.5,4.6,1.5c5.4,0,8.4-4.8,8.4-9c0-0.1,0-0.3,0-0.4	C21.2,11.4,21.7,10.8,22.1,10.2z M14.9,1.5c7.5,0,13.5,6,13.5,13.5s-6,13.5-13.5,13.5S1.4,22.5,1.4,15S7.4,1.5,14.9,1.5z" /></svg>
          </span>
        </div>
      </div>
      <!-- /.ms_medium_container -->
      <img class="dot" src="../../assets/img/icon/o-dot.svg" alt="" />
    </div>
    <!-- /.ms_big_container -->
  </section>
  <!-- /#ms_team -->
</template>

<style lang="scss" scoped>
@use "../../assets/scss/partials/variables" as *;
#ms_team {
  padding: 2rem 0;
  .ms_big_container {
    position: relative;
    padding: 6rem 0;
    .ms_medium_container {
      position: relative;
      .slider_tmp {
        height: 500px;
        width: 50%;
        top: 0;
        left: 0;
        background-color: red;
      }
      .ms_info_member {
        position: absolute;
        top: 50%;
        right: 0;
        transform: translate(0, -50%); //stanlate H
        padding: 5rem 3rem;
        width: 60%;
        svg path {
          fill: $primary;
        }
      }
    }
    .dot {
      position: absolute;
      top: 0;
      right: 0;
    }
  }
}
</style>
