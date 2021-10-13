<template>
  <div>
      <AboutHeader />
      <AboutTestimonial />
      <AboutSubmit />
      <!-- <AboutCTA /> -->
  </div>
</template>
<script>
import AboutHeader from "~/components/AboutHeader.vue";
import AboutTestimonial from "~/components/AboutTestimonial.vue";
import AboutSubmit from "~/components/AboutSubmit.vue";
import AboutCTA from "~/components/AboutCTA.vue";

export default {
  name: "OffersFilter",
  components: {
    AboutHeader,
    AboutTestimonial,
    AboutSubmit,
    AboutCTA
  },
};
</script>
