<script>
import SectionSpecialities from "./SectionSpecialities.vue";
import SectionTeam from "./SectionTeam.vue";
import SectionEvents from "./SectionEvents.vue";
import SectionStats from "./SectionStats.vue";
import SectionBlog from "./SectionBlog.vue";
import SectionTestimonials from "./SectionTestimonials.vue";
import SectionPhoto from "./SectionPhoto.vue";
import SectionContact from "./SectionContact.vue";
import SectionClients from "./SectionClients.vue";
export default {
  name: "PageMain",
  components: {
    SectionSpecialities,
    SectionTeam,
    SectionEvents,
    SectionStats,
    SectionBlog,
    SectionTestimonials,
    SectionPhoto,
    SectionContact,
    SectionClients,
  },
};
</script>
<template>
  <main>
    PageMain
    <SectionSpecialities />
    <SectionTeam />
    <SectionEvents class="bg_dark" />
    <SectionStats />
    <SectionBlog />
    <SectionTestimonials />
    <SectionPhoto />
    <SectionContact />
    <SectionClients />
  </main>
</template>

<style lang="scss" scoped></style>
