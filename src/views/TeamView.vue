<script setup>
import { ref } from 'vue'
import axios from 'axios'
import Card from '../components/CardView.vue'

let teamData = ref([])

axios.get('/data.json').then((response) => {
  teamData.value = response.data.team
})
</script>

<template>
  <main class="main main__background">
    <header class="main__header">
      <h1 class="main__title">Notre Équipe</h1>
    </header>
    <section class="section team__section">
      <Card
        v-for="(item, index) in teamData"
        :key="index"
        :title="item.name"
        :text="item.description"
        :image="item.image"
        type="team"
      />
    </section>
  </main>
</template>
