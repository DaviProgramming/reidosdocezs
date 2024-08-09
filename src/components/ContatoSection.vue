<script setup lang="js">
import { onMounted } from 'vue'
import whatsImage from '../assets/images/zapzap.png'
onMounted(() => {
  let contatoDiv = document.querySelector('#contato')

  contatoDiv.addEventListener('mouseover', (e) => {
    let navbarOptionActive = document.querySelector('nav a.active')
    let navbarOptionToActive = document.querySelector('nav a[href="#contato"]')

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
  <section class="contato" id="contato">
    <div class="custom-shape-divider-top-1722781981">
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
    <div class="contato-container">
      <h1 class="title">Entre em contato e saiba mais!</h1>

      <div class="contato-container-options">
        <div class="option whatsapp">
          <a href="">
            <img :src="whatsImage" alt="" />
          </a>

          <span>Entre em contato conosco pelo WhatsApp</span>
        </div>
      </div>
    </div>
  </section>
</template>
