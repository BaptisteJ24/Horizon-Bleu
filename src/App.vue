<script setup>
import { RouterView } from 'vue-router'
import '@/styles/main.scss'
import Header from '@/components/HeaderLayout.vue'
</script>

<template>
  <Header />
  <RouterView />
</template>
