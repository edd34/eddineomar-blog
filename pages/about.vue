<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="À propos de moi"
      subtitle="Example About Page"
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>Je m'appelle Eddine Omar</h3>
          <p>
            Mon prénom est
            <strong>
              Eddine
            </strong>
            .
          </p>
          <p>
            Je suis originaire de Mayotte, un département français d'Outre-Mer.
            Actuellement, je suis un ingénieur en développement logiciel basé à
            Lyon et diplômé de Polytech 2018. J'adore tout ce qui touche à
            l'ingénierie logicielle, l'IT, la blockchain, le business, l'Open
            Source... J'adore résoudre des problèmes, casse-têtes et puzzles, et
            le développement logiciel permet d'en résoudre plein.
          </p>

          <h3>Pourquoi ce blog ?</h3>
          <p>
            Je me pose souvent des questions sur le monde qui m'entoure, je suis
            quelqu'un de très curieux. Si j'avais un pouvoir, ce serait celui de
            pouvoir tout comprendre. J'ai décidé de créer ce blog afin de
            partager et d'apporter à la communauté de la valeur.
          </p>
          <quote-card />
          <h3></h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci
            eligendi impedit inventore ipsa laboriosam libero magnam modi odio,
            sunt temporibus. Distinctio doloremque eum magni nostrum quasi
            ratione rem repudiandae sit! Lorem ipsum dolor sit amet, consectetur
            adipisicing elit.
            <strong>Alias aut facere harum ipsam</strong> quibusdam quidem
            quisquam saepe? Alias architecto blanditiis consequatur consequuntur
            dicta ipsa iste modi provident, quod, similique veritatis.
          </p>
        </div>

        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Cool Stuff We Do
              </p>
              <p class="subtitle">
                Sooo Cool
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Other Cool Things
              </p>
              <p class="subtitle">
                Just as cool
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                All the cool
              </p>
              <p class="subtitle">
                that is all
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
        </div>
      </template>

      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Derniers posts
        </h3>
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `À propos | ${this.$siteConfig.siteName}`
    }
  },
  components: { QuoteCard }
}
</script>
