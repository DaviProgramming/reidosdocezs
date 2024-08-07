<script setup lang="js">
import { onMounted } from 'vue'
import logo from '../assets/images/logo.png'

onMounted(() => {
  const navbar = document.querySelector('nav')

  window.addEventListener('scroll', () => {
    if (window.scrollY >= 100) {
      if (!navbar.classList.contains('active')) {
        navbar.classList.add('active')
      }
    } else {
      if (navbar.classList.contains('active')) {
        navbar.classList.remove('active')
      }
    }
  })
})
</script>

<template>
  <nav>
    <div class="logo">
      <img :src="logo" alt="" />
      <span>reidosdocezs</span>
    </div>
    <div class="infos">
      <a href="/teste" class="info active">Inicio</a>
      <a href="/teste" class="info">Sobre nós</a>
      <a href="/teste" class="info">Contato</a>
    </div>
  </nav>
</template>
