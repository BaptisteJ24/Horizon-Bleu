<script setup>
import { ref } from 'vue'

const isOpen = ref(false)

const toggleNav = () => {
  isOpen.value = !isOpen.value
  console.log(isOpen.value)
}

const closeNav = () => {
  if (isOpen.value) {
    isOpen.value = false
  }
}
</script>

<template>
  <nav class="nav">
    <button className="nav__btn" v-on:click="toggleNav()">
      <span className="fa-solid fa-bars fa-lg icon-fa">
        <span className="sr-only">Ouvrir le menu de navigation</span>
      </span>
    </button>
    <div className="nav__bar" :data-isopen="isOpen">
      <button className="nav__btn nav__btn--close" v-on:click="toggleNav()">
        <span className="fa-solid fa-xmark fa-lg icon-fa">
          <span className="sr-only">Fermer le menu de navigation</span>
        </span>
      </button>
      <div className="nav__list__container">
        <ul class="nav__list">
          <li class="nav__item">
            <RouterLink class="nav__item__link" to="/news" v-on:click="closeNav()"
              >Actualités</RouterLink
            >
          </li>
          <li class="nav__item">
            <RouterLink class="nav__item__link" to="/activities" v-on:click="closeNav()"
              >Activités</RouterLink
            >
          </li>
          <li class="nav__item">
            <RouterLink class="nav__item__link" to="/rates" v-on:click="closeNav()"
              >Tarifs</RouterLink
            >
          </li>
          <li class="nav__item">
            <RouterLink class="nav__item__link" to="/team" v-on:click="closeNav()"
              >L'équipe</RouterLink
            >
          </li>
          <li class="nav__item">
            <RouterLink class="nav__item__link" to="/about" v-on:click="closeNav()"
              >A propos</RouterLink
            >
          </li>
          <li class="nav__item">
            <RouterLink class="nav__item__link" to="/contact" v-on:click="closeNav()"
              >Contact</RouterLink
            >
          </li>
          <li class="nav__item">
            <RouterLink class="nav__item__link" to="/login" v-on:click="closeNav()">
              <span class="connect-button">
                <span class="mobile-only">Connexion</span>
                <i class="fa-solid fa-right-to-bracket fa-xl"></i>
              </span>
            </RouterLink>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
