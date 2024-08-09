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

  const navbarInfos = document.querySelectorAll('nav .info')

  navbarInfos.forEach((infos) => {
    infos.addEventListener('click', (click) => {
      let infoClicked = click.target

      if (!infoClicked.classList.contains('active')) {
        let infoActived = document.querySelector('.info.active')

        if (infoActived != null) {
          infoActived.classList.remove('active')
        }

        infoClicked.classList.add('active')
      }
    })
  })
})
</script>

<template>
  <nav>
    <div class="logo">
      <a href="">
        <img :src="logo" alt="" />
        <span>reidosdocez</span>
      </a>
    </div>
    <div class="infos">
      <a href="#inicio" class="info active">Inicio</a>
      <a href="#produtos" class="info">Produtos</a>
      <a href="#contato" class="info">Contato</a>
    </div>
  </nav>
</template>
