<script setup></script>

<template>
  <main class="main main__background">
    <header class="main__header">
      <h1 class="main__title">Connexion</h1>
    </header>
    <section class="section login__section">
      <div class="login__content">
        <form class="form text__wrapper login__form">
          <div class="form__content">
            <label class="form__label">
              Identifiant
              <input type="text" placeholder="Identifiant" />
            </label>
            <label class="form__label">
              Mot de passe
              <input type="password" placeholder="Mot de passe" />
            </label>
          </div>
          <button class="button form__button" type="submit" v-on:click="(e) => e.preventDefault()">
            Se connecter
          </button>
        </form>
      </div>
    </section>
  </main>
</template>
