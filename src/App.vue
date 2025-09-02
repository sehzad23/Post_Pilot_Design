<template>
  <div id="app">
    <HeroSection />
    <BrandSection />
    <DirectMail />
    <AppTestimonial />
    <FeaturesGrid />
    <StepsSection />
    <FooterTestimonial />
  </div>
</template>
<script>

import HeroSection from './components/HeroSection.vue';
import BrandSection from './components/BrandSection.vue';
import DirectMail from './components/DirectMail.vue';
import AppTestimonial from './components/AppTestimonial.vue';
import FeaturesGrid from './components/FeaturesGrid.vue';
import StepsSection from './components/StepsSection.vue';
import FooterTestimonial from './components/FooterTestimonial.vue';

export default {

  name: 'App',
  components: {
    HeroSection,
    BrandSection,
    DirectMail,
    AppTestimonial,
    FeaturesGrid,
    StepsSection,
    FooterTestimonial

  }
}
</script>
<style lang="">

</style>