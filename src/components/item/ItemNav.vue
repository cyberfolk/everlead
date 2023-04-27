<script>
export default {
  name: "ItemNav",
  components: {},
};
</script>

<template>
  <nav class="navbar bg-light navbar-expand-lg">
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
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">HOMES</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">PAGES</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">BLOG</a>
          </li>
          <li class="nav-item">
            <a class="nav-link">SHOP</a>
          </li>
          <li class="nav-item">
            <a class="nav-link">EVENTS</a>
          </li>
          <li class="nav-item">
            <a class="nav-link">ELEMENTS</a>
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
    left: -36px;
    font-size: 1.6rem;
    font-weight: 500;
    top: -10%;
  }
}
</style>
