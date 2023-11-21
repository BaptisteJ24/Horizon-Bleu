<script setup>
import { ref } from 'vue'
import axios from 'axios'
import Card from '../components/CardView.vue'

let newsData = ref([])

axios.get('/data.json').then((response) => {
  newsData.value = response.data.news
})
</script>

<template>
  <main class="main main__background">
    <header class="main__header">
      <h1 class="main__title">Nos actualités</h1>
    </header>
    <section class="section news__section">
      <Card
        v-for="(item, index) in newsData"
        :key="index"
        :title="item.title"
        :text="item.text[0]"
        :image="item.image"
        :date="item.date"
        type="news"
      />
    </section>
  </main>
</template>
