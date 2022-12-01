<template>
  <div class="home">
    <intro />
    <pixyz-text />
    <pixyz-service />
    <pixyz-work />
    <pixzy-techno />
    <pixzy-testimonials />
    <get-in-touch />
  </div>
</template>

<script>
import GetInTouch from "../components/GetInTouch.vue";
import Intro from "../components/Intro.vue";
import PixyzService from "../components/PixyzService.vue";
import PixyzText from "../components/PixyzText.vue";
import PixyzWork from "../components/PixyzWork.vue";
import PixzyTechno from "../components/PixzyTechno.vue";
import PixzyTestimonials from "../components/PixzyTestimonials.vue";

export default {
  components: {
    Intro,
    PixyzText,
    PixyzService,
    PixyzWork,
    PixzyTechno,
    PixzyTestimonials,
    GetInTouch,
  },
};
</script>
, GetInTouch
