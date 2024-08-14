<script setup lang="js">
import logo from '../assets/images/logo.png'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faX } from '@fortawesome/free-solid-svg-icons'
</script>

<template>
  <aside>
    <div class="aside-container">
      <div class="aside-header">
        <div class="aside-logo">
          <img :src="logo" alt="" />
        </div>
        <div class="aside-closer">
          <font-awesome-icon :icon="faX" />
        </div>
      </div>
      <div class="aside-body">
        <div class="body-option">Inicio</div>
        <div class="body-option">Produtos</div>
        <div class="body-option">Contato</div>
      </div>
      <div class="aside-footer">rodapé</div>
    </div>
  </aside>
</template>
