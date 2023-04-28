<script>
import navItems from "../../data/nav-item.json";
export default {
  name: "ItemNav",
  data() {
    return {
      navItems: navItems,
      activeLink: 0,
    };
  },
  methods: {
    active(i) {
      this.activeLink = i;
    },
  },
};
</script>

<template>
  <nav class="navbar w-100 navbar-expand-lg">
    <div class="ms_big_container d-flex">
      <a class="navbar-brand" href="#">
        <img width="150" src="../../assets/img/logo/black.png" alt="Logo" class="d-inline-block align-text-top" />
      </a>
      <!-- /.navbar-brand -->
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#main_nav" aria-controls="#main_nav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <!-- /.navbar-toggler -->
      <div class="collapse navbar-collapse justify-content-end" id="main_nav">
        <ul class="navbar-nav">
          <li v-for="(item, i) in navItems" class="nav-item">
            <a class="nav-link" :href="item.path" @click="active(i)" :class="activeLink === i ? 'active' : ''">{{ item.name }}</a>
          </li>
          <li class="nav-item">
            <a class="nav-link"><i class="fa-solid fa-magnifying-glass"></i></a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
@use "../../assets/scss/partials/variables" as *;
nav {
  position: absolute;
  top: 20px;
  left: 0;
  .nav-item {
    font-weight: 700;
    color: $dark !important;
    padding-right: 1.6rem;
    font-size: 0.8rem;
    align-self: center;
    position: relative; // to use the active class

    .active {
      color: $primary;
    }
    .active:after {
      content: "\27F6";
      position: absolute;
      left: -24px;
      font-size: 1.2rem;
      font-weight: 500;
      top: 5%;
    }
  }
}
</style>
