<template>
  <Layout>
    <Showcase/>
    <About/>
    <Services/>
    <Achievements/>
    <Projects/>
    <Feedback/>
    <Pricing/>
    <Gallery/>
  </Layout>
</template>

<script>
import Showcase from "~/components/Showcase.vue";
import About from "~/components/About.vue";
import Services from "~/components/Services.vue";
import Achievements from "~/components/Achievements.vue";
import Projects from "~/components/Projects.vue";
import Feedback from "~/components/Feedback.vue";
import Pricing from "~/components/Pricing.vue";
import Gallery from "~/components/Gallery.vue";

export default {
  metaInfo: {
    title: "Hello!"
  },
  components: {
    Showcase,
    About,
    Services,
    Achievements,
    Projects,
    Feedback,
    Pricing,
    Gallery
  }
  // Work on scrollTo functionality.

  // methods: {
  //   goto(refName) {
  //     var element = this.$refs[refName];
  //     console.log(element);
  //     var top = element.offsetTop;

  //     window.scrollTo(0, top);
  //   }
  // }
};
</script>

<style>
</style>
