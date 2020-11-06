<template>
  <div class="home my-4">
    <v-row class="offset-md-2 col-md-10">
      <v-col
        class="offset-1 offset-md-0 col-md-5 col-9 mb-10"
        align="center"
      >
        <div class="line my-10"></div>
        <h1>Humanizing your insurance.</h1>
        <p class="my-5">
          Get your life insurance coverage easier and faster.
          We blend our expertise and technology to help you find
          the plan that’s right for you. Ensure you and your
          loved ones are protected.
        </p>
        <a href="#">
          <v-btn class="no-border-radius" outlined large dark>
            View plans
          </v-btn>
        </a>
      </v-col>
      <v-col class="offset-md-1">
        <v-img
          src="@/assets/image-intro-desktop.jpg"
          alt="Intro"
          class="intro-img"
        ></v-img>
      </v-col>
    </v-row>
    <v-img
      src="@/assets/bg-pattern-intro-right-desktop.svg"
      alt="Background Right"
      class="pattern-right"
    ></v-img>
    <v-img
      src="@/assets/bg-pattern-intro-left-desktop.svg"
      alt="Background Left"
      class="pattern-left"
    ></v-img>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>

<style lang="css" scoped>

@media only screen and (max-width: 600px) {
  .intro-img {
    position: relative !important;
    top: 0 !important;
    left: 1.5vh;
}
}

.home {
  background-color: var(--dark-violet) !important;
  color: white;
}
.intro-img {
  width: 50vh;
  position: relative;
  top: 18vh;
}
.line {
  border-top: 1px solid white;
  width: 20%;
}
.pattern-right {
  position: absolute;
  top: 12vh;
  right: 0;
  width: 25%;
}
.pattern-left {
  position: absolute !important;
  top: 50vh;
  left: 0;
  width: 15%;
}
h1 {
  font-family: "DMSerif" !important;
  font-weight: 500 !important;
  font-size: 3.75rem;
}
p {
  font-family: "Karla" !important;
}
a {
  text-decoration: none !important;
}
.no-border-radius {
  border-radius: 0 !important;
}
</style>
