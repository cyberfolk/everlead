<script>
import header from "./data/header.json";
import PageHeader from "./components/PageHeader.vue";
import PageMain from "./components/PageMain.vue";
import PageFooter from "./components/PageFooter.vue";
export default {
  components: {
    PageHeader,
    PageMain,
    PageFooter,
  },
  data() {
    return { header: header };
  },
};
</script>

<template>
  <PageHeader :logoPath="header.logoPath" :navItems="header.navItems"></PageHeader>
  <PageMain></PageMain>
  <PageFooter></PageFooter>
</template>

<style lang="scss" scoped></style>
