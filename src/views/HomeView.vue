<script setup>
import HeroHome from '@/components/HeroHome.vue'
import Loader from '@/components/Loader.vue'
import Navbar from '@/components/Navbar.vue'
import ProductsSection from '@/components/ProductsSection.vue'
import showProducts from '@/components/showProducts.vue'
</script>

<template>
  <Loader />
  <Navbar />
  <HeroHome />
  <ProductsSection />
  <showProducts />
</template>
