<script setup>
import { ref } from 'vue'
import axios from 'axios'

let ratesData = ref([])

axios.get('/data.json').then((response) => {
  ratesData.value = response.data.rates
})
</script>

<template>
  <main class="main main__background">
    <header class="main__header rates__main__header">
      <h1 class="main__title">Nos Tarifs</h1>
      <div class="button__wrapper">
        <button class="button">Simuler ma venue</button>
        <button class="button">Réserver mon emplacement</button>
      </div>
    </header>
    <section class="section rates__section">
      <table class="text__wrapper table" v-for="(item, index) in ratesData" :key="index">
        <thead class="table__content">
          <tr class="tr">
            <th class="th">{{ item.header }}</th>
            <th class="th">Tarif par nuitée</th>
          </tr>
        </thead>
        <tbody class="table__content">
          <tr v-for="(item, index) in item.data" :key="index" class="tr">
            <td class="td">{{ item.title }}</td>
            <td class="td">{{ item.price }}</td>
          </tr>
        </tbody>
      </table>
    </section>
  </main>
</template>
