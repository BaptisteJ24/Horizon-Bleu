<script setup>
import Background from '@/assets/images/homepage.jpg'
import axios from 'axios'
import { ref } from 'vue'
</script>

<script>
let homepageData = ref([])

import { getImagePath } from '@/utils/utils'

axios.get('/data.json').then((response) => {
  homepageData.value = response.data.homepage
})
</script>

<template>
  <main class="main homepage__main">
    <header class="main__header">
      <img :src="Background" alt="background" class="main__img" />
      <div class="main__header__content">
        <h1 class="homepage__title">
          Bienvenue au camping Horizon Bleu, votre oasis en bord de mer !
        </h1>
        <h2 class="homepage__subtitle">
          Créez des souvenirs et laissez les vagues emporter vos soucis.
        </h2>
      </div>
      <a href="/#main-section" aria-hidden="true" class="main__header__next-section">
        <span class="sr-only">Scroll to next section</span>
        <i class="fas fa-chevron-down fa-2xl" />
        <i class="fas fa-chevron-down fa-2xl" />
      </a>
    </header>
    <section class="main__section" id="main-section">
      <article class="article homepage__article" v-for="(item, index) in homepageData" :key="index">
        <div class="article__content">
          <h2 class="article__title">{{ item.title }}</h2>
          <p class="article__text" v-for="(text, index) in item.text" :key="index">
            {{ text }}
          </p>
        </div>
        <div class="article__picture__wrapper">
          <div class="article__picture">
            <img :src="getImagePath(item.image)" :alt="item.image" />
          </div>
        </div>
      </article>
    </section>
  </main>
</template>
