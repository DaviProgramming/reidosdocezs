<script setup>
import HeroHome from '@/components/HeroHome.vue'
import Loader from '@/components/Loader.vue'
import Navbar from '@/components/Navbar.vue'
import ProductsSection from '@/components/ProductsSection.vue'
import ContatoSection from '@/components/ContatoSection.vue'
import FooterComponent from '@/components/Footer.vue'
import Aside from '@/components/Aside.vue'
</script>

<template>
  <Loader />
  <Navbar />
  <HeroHome />
  <ProductsSection />
  <ContatoSection />
  <FooterComponent />
</template>
