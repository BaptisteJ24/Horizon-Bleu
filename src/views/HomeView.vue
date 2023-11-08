<script setup>
import Background from '@/assets/images/homepage.jpg'
</script>

<template>
  <main class="main">
    <header class="main__header">
      <img :src="Background" alt="background" class="main__img" />
      <div class="main__header__content">
        <h1 class="main__title">Bienvenue au camping Horizon Bleu, votre oasis en bord de mer !</h1>
        <h2 class="main__subtitle">
          Créez des souvenirs et laissez les vagues emporter vos soucis.
        </h2>
      </div>
      <a href="/#welcome" aria-hidden="true">
        <div class="main__header__next-section">
          <span class="sr-only">Scroll to next section</span>
          <i class="fas fa-chevron-down fa-2xl"></i>
          <i class="fas fa-chevron-down fa-2xl"></i>
        </div>
      </a>
    </header>
    <section class="main__section" id="welcome" v-on:click="onTransitionStart">
      <div class="main__section__content">
        <article>
          <h2 class="section__title">Bienvenue au Camping Horizon Bleu</h2>
          <p class="section__text">
            Nous sommes ouvert toute l'année, n'hésitez pas à nous contacter pour réserver votre
            séjour.
          </p>
          <p class="section__text">
            Niché au cœur d'un paysage côtier spectaculaire, notre camping offre une expérience
            unique pour les amateurs de plein air, les familles et les amis en quête d'aventures
            mémorables. Situé sur les rives de l'océan, notre camping vous accueille avec des vues à
            couper le souffle, des plages de sable fin et une atmosphère chaleureuse. Nous sommes
            impatients de vous accueillir !
          </p>
        </article>
        <article>
          <h2 class="section__title">Découvrez la Beauté de la Mer</h2>
          <p>
            Découvrez la Beauté de la Mer Imaginez-vous vous réveiller au son des vagues douces
            caressant le rivage, sentir la brise marine sur votre visage et admirer le lever du
            soleil sur l'horizon infini de l'océan. Au Camping Horizon Bleu, vous pourrez vous
            détendre sur nos plages privées, explorer des criques cachées, et profiter de baignades
            rafraîchissantes dans les eaux cristallines de la mer. Les amateurs de sports nautiques
            trouveront leur bonheur avec une gamme d'activités telles que le surf, la plongée, et le
            kayak.
          </p>
        </article>
        <article>
          <h2 class="section__title">Une Expérience de Camping Inoubliable</h2>
          <p>
            Notre camping propose des emplacements spacieux pour tentes, caravanes et camping-cars,
            offrant un accès facile à la plage et aux installations. Que vous soyez un campeur
            chevronné ou un débutant, notre équipe chaleureuse est là pour rendre votre séjour
            agréable et sans soucis. Profitez de notre aire de jeux pour enfants, découvrez nos
            sentiers de randonnée pittoresques et détendez-vous autour d'un feu de camp sous un ciel
            étoilé.
          </p>
        </article>
        <article>
          <h2 class="section__title">Découvrez la Cuisine Locale</h2>
          <p>
            Savourez la cuisine locale et les délices de la mer dans notre restaurant en bord de
            mer. Dégustez des fruits de mer frais, des spécialités régionales et des plats préparés
            avec amour par nos chefs talentueux. Profitez de repas en plein air avec vue sur l'océan
            et découvrez les saveurs uniques de la région.
          </p>
        </article>
        <article>
          <h2 class="section__title">Réserver Votre Aventure au Camping Horizon Bleu</h2>
          <p>
            Que vous soyez à la recherche d'une escapade romantique au bord de la mer, d'une
            aventure en famille ou d'une pause détente entre amis, le Camping Horizon Bleu vous
            promet des moments inoubliables dans un cadre naturel exceptionnel. Réservez dès
            maintenant et laissez-vous séduire par l'ambiance relaxante et la magie de l'océan.
            Venez créer des souvenirs inoubliables au Camping Horizon Bleu, votre destination de
            camping par excellence au bord de la mer.
          </p>
        </article>
      </div>
    </section>
  </main>
</template>
