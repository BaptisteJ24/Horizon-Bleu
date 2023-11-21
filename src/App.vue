<script setup>
import { RouterView } from 'vue-router'
import '@/styles/main.scss'
import Header from '@/components/HeaderLayout.vue'
import Footer from '@/components/FooterLayout.vue'
</script>

<template>
  <Header />
  <RouterView />
  <Footer />
</template>
