<template>
  <div class="tm-page">
    <NavBar />
    <!-- <Buttons /> -->
    <Nuxt />
    <Footer />
  </div>
</template>

<script>
import NavBar from './../components/Navbar'
import Footer from './../components/Footer'
import Buttons from './../components/Buttons'

export default {
  components: {
    NavBar,
    Footer,
    Buttons
  }
}
</script>

<style>
  body, h1, h2,h3, span, p, div, a {
    font-family: 'Montserrat' serif !important;
  }
</style>