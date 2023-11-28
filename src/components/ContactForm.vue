<template>
  <form class="form text__wrapper">
    <div class="form__content">
      <label class="form__label">
        Prénom
        <input type="text" placeholder="Prénom" />
      </label>
      <label class="form__label">
        Nom de famille
        <input type="text" placeholder="Nom de famille" />
      </label>
    </div>
    <label class="form__label">
      Email *
      <input type="text" placeholder="contact@exemple.com" />
    </label>
    <label class="form__label">
      Objet du message
      <input type="text" placeholder="Mail depuis le site" />
    </label>
    <label class="form__label">
      Message *
      <textarea placeholder="Votre message..."></textarea>
    </label>
    <button class="button form__button" type="submit" v-on:click="(e) => e.preventDefault()">
      Envoyer
    </button>
    <p class="info">
      * Ce site étant fictif, les informations de contact sont elles aussi fictives. Ce formulaire
      n'est donc pas fonctionnel. Si vous souhaitez tout de même me contacter, vous pouvez le faire
      via le site :
      <a
        href="https://baptiste-jan.fr/#contact"
        class="info__link"
        target="_blank"
        rel="norefferer"
      >
        baptiste-jan.fr </a
      >, ou par mail à l'adresse :
      <a href="mailto:contact@baptiste-jan.fr" class="info__link">contact@baptiste-jan.fr</a>.
    </p>
  </form>
</template>
