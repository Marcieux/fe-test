<template>
  <div>
    <Navbar />
    <HeroSection />
    <CategorySection />
    <AboutSection />
    <ProductCatalog />
    <FooterSection />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import HeroSection from './components/HeroSection.vue'
import CategorySection from './components/CategorySection.vue'
import AboutSection from './components/AboutSection.vue'
import ProductCatalog from './components/ProductCatalog.vue'
import FooterSection from './components/FooterSection.vue'


export default {
  components: {
    Navbar,
    HeroSection,
    CategorySection,
    AboutSection,
    ProductCatalog,
    FooterSection
  }
}
</script>
