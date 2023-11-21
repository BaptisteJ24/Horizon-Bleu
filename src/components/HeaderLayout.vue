<script setup>
import { RouterLink } from 'vue-router'
import Logo from '@/assets/logo.png'
</script>

<template>
  <header class="header">
    <div className="logo">
      <RouterLink to="/" class="logo__link">
        <img :src="Logo" alt="logo Horizon Bleu" class="logo__img" />
        <span>Horizon Bleu</span>
      </RouterLink>
    </div>
    <nav class="nav">
      <ul class="nav__list">
        <li class="nav__item">
          <RouterLink class="nav__item__link" to="/news">Actualités</RouterLink>
        </li>
        <li class="nav__item">
          <RouterLink class="nav__item__link" to="/activities">Activités</RouterLink>
        </li>
        <li class="nav__item">
          <RouterLink class="nav__item__link" to="/rates">Tarifs</RouterLink>
        </li>
        <li class="nav__item">
          <RouterLink class="nav__item__link" to="/team">L'équipe</RouterLink>
        </li>
        <li class="nav__item">
          <RouterLink class="nav__item__link" to="/about">A propos</RouterLink>
        </li>
        <li class="nav__item">
          <RouterLink class="nav__item__link" to="/contact">Contact</RouterLink>
        </li>
        <li class="nav__item">
          <RouterLink class="nav__item__link" to="/connexion">
            <span class="connect-button">
              <span class="sr-only">Connexion</span>
              <i class="fa-solid fa-right-to-bracket fa-xl"></i>
            </span>
          </RouterLink>
        </li>
      </ul>
    </nav>
  </header>
</template>
