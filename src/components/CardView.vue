<script setup>
defineProps({
  title: String,
  text: String,
  image: String,
  date: String,
  type: String
})

import { getImagePath } from '@/utils/utils'
</script>

<template>
  <article v-if="type === 'news'" class="card">
    <div class="card__picture">
      <img :src="getImagePath(image)" :alt="image" loading="lazy" />
    </div>
    <div class="card__content">
      <h2 class="card__title">{{ title }}</h2>
      <p class="card__text">
        {{ text }}
      </p>
      <p class="card__text">Posté le : {{ date }}</p>
    </div>
  </article>
  <article v-else-if="type === 'team'" class="card card--team">
    <div class="card__picture">
      <img :src="getImagePath(image)" :alt="image" loading="lazy" />
    </div>
    <div class="card__content">
      <h2 class="card__title">{{ title }}</h2>
      <p class="card__text">
        {{ text }}
      </p>
    </div>
  </article>
  <div v-else-if="type === 'activities'" class="card card--activities">
    <div class="card__picture">
      <img :src="getImagePath(image)" :alt="image" loading="lazy" />
    </div>
  </div>
</template>
