<script setup>
import { ref } from 'vue'
import axios from 'axios'

let aboutData = ref([])

axios.get('/data.json').then((response) => {
  aboutData.value = response.data.about
})
</script>

<template>
  <main class="main main__background">
    <header class="main__header">
      <h1 class="main__title">A Propos de Nous</h1>
    </header>
    <section class="section about__section">
      <div class="text__wrapper">
        <p v-for="(item, index) in aboutData.message" :key="index">{{ item }}</p>
      </div>
      <div class="text__wrapper">
        <p>{{ aboutData.services.title }}</p>
        <ul v-for="(item, index) in aboutData.services.items" :key="index">
          <li class="bullet">{{ item }}</li>
        </ul>
      </div>
    </section>
  </main>
</template>
