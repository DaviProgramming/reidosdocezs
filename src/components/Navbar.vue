<script setup>
import logo from '../assets/images/logo.png'
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
