<template>
  <div id="app">
    <HeroSection />
    <BrandSection />
    <DirectMail />
    <AppTestimonial />
  </div>
</template>
<script>

import HeroSection from './components/HeroSection.vue';
import BrandSection from './components/BrandSection.vue';
import DirectMail from './components/DirectMail.vue';
import AppTestimonial from './components/AppTestimonial.vue';

export default {

  name: 'App',
  components: {
    HeroSection,
    BrandSection,
    DirectMail,
    AppTestimonial

  }
}
</script>
<style lang="">

</style>