<template>
  <div id="contact-page" class="page-wrapper contact-page content-page">
    <site-hero
      title="Contactez moi"
      subtitle="Je vous répondrai très rapidement"
      image="/uploads/contact-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Salut !
              </p>
              <p class="subtitle">
                Une question, une remarque ? N'hésitez pas, je serai ravis de
                vous répondre 🙂
              </p>
              <figure class="image is-1by1 ">
                <opti-image
                  :src="require('~/assets/uploads/contact-person.jpg').src"
                  :srcset="
                    require('~/assets/uploads/contact-person.jpg').srcSet
                  "
                />
              </figure>
              <br />
              <div class="content">
                <p>
                  <strong>
                    "Skills are cheap, passion is priceless" (Gary Vaynerchuck)
                  </strong>
                </p>
                <p>
                  Passionné de l'ingénierie logicielle, l'IT, la tech,l'Open
                  Source, le business... mais aussi curieux, autodidacte, j'ai
                  décidé de créer ce blog afin de partager sur les sujets qui
                  m'intéressent.
                </p>
              </div>
            </article>
          </div>
          <div class="tile is-parent is-8">
            <article class="tile is-child box">
              <contact-form />
            </article>
          </div>
        </div>
      </template>
      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Derniers posts
        </h3>
        <!-- Latest Posts -->
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import ContactForm from '~/components/ContactForm'
export default {
  head() {
    return {
      title: `Contact | ${this.$siteConfig.siteName}`
    }
  },
  components: { ContactForm }
}
</script>
