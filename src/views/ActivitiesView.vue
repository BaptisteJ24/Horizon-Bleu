<script setup>
import { ref } from 'vue'
import axios from 'axios'
import Card from '@/components/CardView.vue'

let newsData = ref([])

axios.get('/data.json').then((response) => {
  newsData.value = response.data.activities
})
</script>

<template>
  <main class="main main__background">
    <header class="main__header">
      <h1 class="main__title">Nos activités</h1>
    </header>
    <section class="section activities__section">
      <div>
        <p class="text__wrapper">{{ newsData.intro }}</p>
      </div>
      <article
        v-for="(item, index) in newsData.data"
        :key="index"
        class="article activities__article"
      >
        <Card :image="item.image" type="activities" />
        <div class="text__wrapper">
          <h2 class="article__title">{{ item.title }}</h2>
          <p class="article__text">{{ item.text }}</p>
        </div>
      </article>
    </section>
  </main>
</template>
