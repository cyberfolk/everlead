<script>
import SectionJumbotron from "./section/SectionJumbotron.vue";
import SectionSpecialities from "./section/SectionSpecialities.vue";
import SectionTeam from "./section/SectionTeam.vue";
import SectionEvents from "./section/SectionEvents.vue";
import SectionStats from "./section/SectionStats.vue";
import SectionBlog from "./section/SectionBlog.vue";
import SectionTestimonials from "./section/SectionTestimonials.vue";
import SectionPhotos from "./section/SectionPhotos.vue";
import SectionContact from "./section/SectionContact.vue";
import SectionClients from "./section/SectionClients.vue";
export default {
  name: "PageMain",
  components: {
    SectionJumbotron,
    SectionSpecialities,
    SectionTeam,
    SectionEvents,
    SectionStats,
    SectionBlog,
    SectionTestimonials,
    SectionPhotos,
    SectionContact,
    SectionClients,
  },
};
</script>
<template>
  <main>
    <SectionJumbotron />
    <SectionSpecialities />
    <SectionTeam />
    <SectionEvents />
    <SectionStats />
    <SectionBlog />
    <SectionTestimonials />
    <SectionPhotos />
    <SectionContact />
    <SectionClients />
  </main>
</template>

<style lang="scss" scoped></style>
