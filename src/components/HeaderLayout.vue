<script setup>
import { RouterLink } from 'vue-router'
import Nav from '@/components/NavView.vue'
import Logo from '@/assets/logo.png'
</script>

<template>
  <header class="header">
    <div className="logo">
      <RouterLink to="/" class="logo__link">
        <img :src="Logo" alt="logo Horizon Bleu" class="logo__img" />
        <span>Horizon Bleu</span>
      </RouterLink>
    </div>
    <Nav />
  </header>
</template>
