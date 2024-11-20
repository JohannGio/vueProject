<template>
  <div class="w-screen">
    <NavBar />
    <HeroSection />
    <ShortenSection />
    <StatsSection />
    <FeatureBoxSection />
    <Cta />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import HeroSection from './components/HeroSection.vue';
import ShortenSection from './components/ShortenSection.vue';
import StatsSection from './components/StatsSection.vue';
import Footer from './components/Footer.vue';
import FeatureBoxSection from './components/FeatureBoxSection.vue';
import NavBar from './components/NavBar.vue';
import Cta from './components/Cta.vue';

export default {
  name: 'App',
  components: {
    Header,
    HeroSection,
    ShortenSection,
    Footer,
    StatsSection,
    NavBar,
    Cta,
  },
};
</script>
