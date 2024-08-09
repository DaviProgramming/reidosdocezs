<script setup lang="ts">
import imageHero from '../assets/images/bolo.jpg'
import product1 from '../assets/images/bolo-de-pote.png'
import product2 from '../assets/images/caixa-de-doces.png'

import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { byPrefixAndName } from '@awesome.me/kit-KIT_CODE/icons'
import { faInstagram, faTiktok } from '@fortawesome/free-brands-svg-icons'
import { onMounted } from 'vue'

onMounted(() => {
  let inicioDiv = document.querySelector('#inicio')

  inicioDiv.addEventListener('mouseover', (e) => {
    let navbarOptionActive = document.querySelector('nav a.active')
    let navbarOptionToActive = document.querySelector('nav a[href="#inicio"]')

    if (navbarOptionActive != null) {
      navbarOptionActive.classList.remove('active')
    }

    if (!navbarOptionToActive.classList.contains('active')) {
      navbarOptionToActive.classList.add('active')
    }
  })
})
</script>

<template>
  <section class="container-hero" id="inicio">
    <div class="container-hero-texts-infos">
      <div class="containe-hero-texts-infos-title">
        <span>Sabor real </span> <span>em</span>
        <span>cada mordida</span>
        <div class="containe-hero-texts-infos-redes">
          <div class="rede-social">
            <a href="https://www.instagram.com/reidosdocez/" target="_blank">
              <font-awesome-icon :icon="faInstagram" />
            </a>
          </div>
        </div>
      </div>
    </div>

    <div class="container-hero-products">
      <div class="product">
        <img :src="product2" alt="" />
      </div>
      <div class="product blur">
        <img :src="product2" alt="" />
      </div>
    </div>

    <div class="container-hero-image">
      <!-- <img :src="imageHero" alt="" /> -->
    </div>
    <div class="custom-shape-divider-bottom-1722781356">
      <svg
        data-name="Layer 1"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 1200 120"
        preserveAspectRatio="none"
      >
        <path
          d="M985.66,92.83C906.67,72,823.78,31,743.84,14.19c-82.26-17.34-168.06-16.33-250.45.39-57.84,11.73-114,31.07-172,41.86A600.21,600.21,0,0,1,0,27.35V120H1200V95.8C1132.19,118.92,1055.71,111.31,985.66,92.83Z"
          class="shape-fill"
        ></path>
      </svg>
    </div>
  </section>
</template>
