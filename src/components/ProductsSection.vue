<script setup lang="js">
import bolo from '../assets/images/bolo.png'
import boloPote from '../assets/images/bolo-de-pote.png'
import caixaDoce from '../assets/images/caixa-de-doces.png'
import boloMorango from '../assets/images/bolo2.png'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faArrowLeft, faArrowRight } from '@fortawesome/free-solid-svg-icons'

import { onMounted } from 'vue'

onMounted(() => {
  const prevButton = document.querySelector('.prev-button')
  const nextButton = document.querySelector('.next-button')

  const imgSlider = document.querySelector('.img-slider')

  const allImages = document.querySelectorAll('.img-item')

  const infoItemAll = document.querySelectorAll('.info-item')

  let indexSlider = 0
  let index = 0
  let indexInfo = 0

  nextButton.addEventListener('click', () => {
    indexSlider++

    imgSlider.style.transform = `rotate(${indexSlider * -90}deg)`
    index++

    if (index > allImages.length - 1) {
      index = 0
    }

    indexInfo++

    if (indexInfo > infoItemAll.length - 1) {
      indexInfo = 0
    }

    let activeInfoItem = document.querySelector('.info-item.active')

    if (activeInfoItem != null) {
      activeInfoItem.classList.remove('active')
    }

    infoItemAll[indexInfo].classList.add('active')
  })

  prevButton.addEventListener('click', () => {
    indexSlider--

    imgSlider.style.transform = `rotate(${indexSlider * -90}deg)`
    index--

    if (index < 0) {
      index = 0
    }

    indexInfo--

    if (indexInfo < 0) {
      indexInfo = infoItemAll.length - 1
    }

    let activeInfoItem = document.querySelector('.info-item.active')

    if (activeInfoItem != null) {
      activeInfoItem.classList.remove('active')
    }

    infoItemAll[indexInfo].classList.add('active')
  })

  let produtosDiv = document.querySelector('#produtos')

  produtosDiv.addEventListener('mouseover', (e) => {
    let navbarOptionActive = document.querySelector('nav a.active')
    let navbarOptionToActive = document.querySelector('nav a[href="#produtos"]')

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
  <section class="products" id="produtos">
    <h1>Produtos</h1>
    <div class="container-produtos">
      <div class="carousel">
        <div class="img-box">
          <div class="img-list">
            <div class="img-slider">
              <div class="img-item" style="--i: 0">
                <img :src="bolo" alt="" />
              </div>
              <div class="img-item" style="--i: 1">
                <img :src="boloPote" alt="" />
              </div>
              <div class="img-item" style="--i: 2">
                <img :src="caixaDoce" alt="" />
              </div>
              <div class="img-item" style="--i: 3">
                <img :src="boloMorango" alt="" />
              </div>
            </div>
          </div>
        </div>

        <div class="info-box">
          <div class="info-slider">
            <div class="info-item active">
              <h2>Bolo de chocolate com ninho</h2>
              <p>
                Descubra o prazer de nosso bolo de chocolate, com uma massa rica e fofinha. Coberto
                com um cremoso creme de ninho e decorado com morangos frescos, oferece uma
                combinação perfeita de sabores e texturas.
              </p>
            </div>
            <div class="info-item">
              <h2>Bolo de pote de chocolate e chantilly</h2>
              <p>
                Delicie-se com nosso bolo de pote de chocolate: massa rica e macia, combinada com
                chantilly cremoso. Cada camada é uma explosão de sabor, finalizada com raspas de
                chocolate. A sobremesa perfeita para um toque doce e especial!
              </p>
            </div>
            <div class="info-item">
              <h2>Caixa de bombom de chocolate e ninho</h2>
              <p>
                nossa caixa de bombons combina o melhor do chocolate com o cremoso sabor de ninho.
                Uma verdadeira experiência gourmet que vai encantar seu paladar e tornar qualquer
                momento ainda mais especial.
              </p>
            </div>
            <div class="info-item">
              <h2>Bolo de chocolate de chocolate com morangos</h2>
              <p>
                nosso bolo de chocolate é feito com uma massa fofinha e rica, coberta com um ganache
                de chocolate irresistível e enfeitado com morangos frescos. É a combinação perfeita
                de chocolate e frutas que vai deixar qualquer momento ainda mais especial e
                delicioso
              </p>
            </div>
          </div>
        </div>

        <div class="navigation">
          <div class="prev-button"><font-awesome-icon :icon="faArrowLeft" /></div>
          <div class="next-button"><font-awesome-icon :icon="faArrowRight" /></div>
        </div>
      </div>
    </div>
  </section>
</template>
