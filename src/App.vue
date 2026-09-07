<template>
  <div class="min-h-screen bg-white text-slate-900">
    <SiteNavbar />

    <main>
      <HeroSection />
      <AboutSection />
      <GetItSoldSection />
      <PropertiesSection />
      <AffiliationSection />
      <GallerySection />
      <ServicesSection />
      <SocialMediaSection />
      <ContactSection />
      <MapSection />
    </main>

    <SiteFooter />

  </div>
</template>
<script setup lang="ts">
import SiteNavbar from './components/home/SiteNavbar.vue'
import HeroSection from './components/home/HeroSection.vue'
import SiteFooter from './components/home/SiteFooter.vue'
import AboutSection from './components/home/AboutSection.vue'
import GetItSoldSection from './components/home/GetItSoldSection.vue'
import PropertiesSection from './components/home/PropertiesSection.vue'
import AffiliationSection from './components/home/AffiliationSection.vue'
import GallerySection from './components/home/GallerySection.vue'
import ServicesSection from './components/home/ServicesSection.vue'
import SocialMediaSection from './components/home/SocialMediaSection.vue'
import ContactSection from './components/home/ContactSection.vue'
import MapSection from './components/home/MapSection.vue'

</script>
