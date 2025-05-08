<template>
  <div id="app">
    <Navbar />
    <HeroSection />
    <AboutSection />
    <ServicesSection />
    <ContactSection />
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import ServicesSection from './components/ServicesSection.vue'
import ContactSection from './components/ContactSection.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    HeroSection,
    AboutSection,
    ServicesSection,
    ContactSection,
    Footer
  }
}
</script>

<style>
/* Gaya global */
body {
  font-family: 'Arial', sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.6;
}

.container {
  width: 85%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px 0;
}

section {
  padding: 60px 0;
}

h1, h2, h3 {
  color: #2c3e50;
}
</style>