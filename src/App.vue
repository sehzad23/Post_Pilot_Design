<template>
  <div id="app">
    <HeroSection />
    <BrandSection />
    <DirectMail />
    <AppTestimonial />
    <FeaturesGrid />
    <StepsSection />
    <FooterTestimonial />
    <CaseStudySection />
    <PostPilotSection />
    <LatestTrends />
    <AppFooter />
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
import CaseStudySection from './components/CaseStudySection.vue';
import PostPilotSection from './components/PostPilotSection.vue';
import LatestTrends from './components/LatestTrends.vue';
import AppFooter from './components/AppFooter.vue';

export default {

  name: 'App',
  components: {
    HeroSection,
    BrandSection,
    DirectMail,
    AppTestimonial,
    FeaturesGrid,
    StepsSection,
    FooterTestimonial,
    CaseStudySection,
    PostPilotSection,
    LatestTrends,
    AppFooter

  }
}
</script>
<style lang="">

</style>