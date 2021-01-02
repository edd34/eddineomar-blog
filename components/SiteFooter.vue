<template>
  <footer class="site-footer">
    {{ $siteConfig.siteName }} &copy; {{ new Date().getFullYear() }} - Tous
    drois réservés
    <br />
    Conçus avec <span style="color: #e25555;">&#9829;</span> grâce à Nuxt.js et
    Netlify. Inspiré du template
    <a href="https://templates.netlify.com/template/awake-blog-template-nuxt/">
      Awake
    </a>
  </footer>
</template>

<script>
export default {
  name: 'SiteFooter'
}
</script>

<style scoped>
footer {
  background: #eee;
  padding: 20px 10px;
  text-align: center;
  transition: 0.5s ease all;
}
</style>
