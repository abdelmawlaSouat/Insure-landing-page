<template>
  <v-app>
    <v-main>
      <NavBar />
      <Home />
      <AboutUs />
      <Footer />
    </v-main>
  </v-app>
</template>

<script>
import NavBar from './components/NavBar'
import Home from './components/Home'
import AboutUs from './components/AboutUs'
import Footer from './components/Footer'

export default {
  name: 'App',
  components: {
    NavBar, Home, AboutUs, Footer
  }
}
</script>

<style lang="css">

@font-face {
  font-family: "Karla";
  src: local("Karla"),
    url(./fonts/Karla-Regular.ttf) format("truetype");
}
@font-face {
  font-family: "DMSerif";
  src: local("DMSerif"),
    url(./fonts/DMSerifDisplay-Regular.ttf) format("truetype");
}

:root {
  --dark-violet: hsl(256, 26%, 20%);
}
</style>
