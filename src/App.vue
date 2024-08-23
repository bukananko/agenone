<script setup lang="ts">
import Navbar from "./components/Navbar.vue";
import Hero from "./components/Hero/index.vue";
import Services from "./components/Services.vue";
import Achievement from "./components/Achievement.vue";
import OurWorks from "./components/OurWorks.vue";
import TrustedCompany from "./components/TrustedCompany.vue";
import Testimonials from "./components/Testimonials.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
  <Navbar />
  <main>
    <Hero />
    <Services />
    <Achievement />
    <OurWorks />
    <TrustedCompany />
    <Testimonials />
  </main>
  <Footer />
</template>
