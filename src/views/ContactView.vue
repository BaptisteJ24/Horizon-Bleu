<script setup>
import { ref } from 'vue'
import axios from 'axios'
import ContactForm from '../components/ContactForm.vue'
import Logo from '@/assets/logo.png'

let contactData = ref([])

axios.get('/data.json').then((response) => {
  contactData.value = response.data.contact
})
</script>

<template>
  <main class="main main__background">
    <header class="main__header">
      <h1 class="main__title">Nous contacter</h1>
    </header>
    <section class="section contact__section">
      <div class="contact__content">
        <ContactForm />
        <aside class="contact__aside text__wrapper">
          <div class="contact__aside__header">
            <img :src="Logo" alt="logo" />
            <h2 class="contact__aside__title"><span>Camping</span><span>Horizon Bleu</span></h2>
          </div>
          <h5 class="contact__aside__label">Téléphone :</h5>
          <p class="contact__aside__text">
            <a href="tel:+33 1 23 45 67 89">+33 1 23 45 67 89</a>
          </p>
          <h5 class="contact__aside__label">Email :</h5>
          <p class="contact__aside__text">
            <a href="mailto:contact@horizon-bleu.fr"> contact@horizon-bleu.fr </a>
          </p>
        </aside>
      </div>
    </section>
  </main>
</template>
