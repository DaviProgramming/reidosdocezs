<script setup lang="js">
import { onMounted, ref } from 'vue'
import logo from '../assets/images/logo.png'

const isLoading = ref(true)

onMounted(() => {
  isLoading.value = false

  let body = document.body

  if (body.classList.contains('loader')) {
    body.classList.remove('loader')
  }
})
</script>

<template>
  <section v-if="isLoading" class="loader">
    <div class="loader-container">
      <div class="logo">
        <img :src="logo" alt="" />
      </div>
    </div>
  </section>
</template>
