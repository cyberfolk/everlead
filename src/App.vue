<script>
import SiteHeader from "./components/PageHeader .vue";
import SiteMain from "./components/PageMain.vue";
import SiteFooter from "./components/PageFooter.vue";
export default {
  components: {
    SiteHeader,
    SiteMain,
    SiteFooter,
  },
};
</script>

<template>
  <PageHeader></PageHeader>
  <PageMain></PageMain>
  <PageFooter></PageFooter>
</template>

<style lang="scss" scoped></style>
