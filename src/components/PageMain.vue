<script>
import SectionSpecialities from "./section/SectionSpecialities.vue";
import SectionTeam from "./section/SectionTeam.vue";
import SectionEvents from "./section/SectionEvents.vue";
import SectionStats from "./section/SectionStats.vue";
import SectionBlog from "./section/SectionBlog.vue";
import SectionTestimonials from "./section/SectionTestimonials.vue";
import SectionPhoto from "./section/SectionPhoto.vue";
import SectionContact from "./section/SectionContact.vue";
import SectionClients from "./section/SectionClients.vue";
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
    <SectionSpecialities />
    <SectionTeam />
    <SectionEvents />
    <SectionStats />
    <SectionBlog />
    <SectionTestimonials />
    <SectionPhoto />
    <SectionContact />
    <SectionClients />
  </main>
</template>

<style lang="scss" scoped></style>
