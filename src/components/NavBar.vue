<template>
  <v-container>
    <v-app-bar flat color="white">
      <img
        src="@/assets/logo.svg"
        alt="Insure Logo"
        width="150"
      >
      <v-spacer></v-spacer>

      <!-- Buttons List -->
      <a href="#">
        <v-btn class="mr-2" text large>
          How We work
        </v-btn>
      </a>
      <a href="#">
        <v-btn class="mr-2" text large>
          Blog
        </v-btn>
      </a>
      <a href="#">
        <v-btn class="mr-2" text large>
          Account
        </v-btn>
      </a>
      <a href="#">
        <v-btn
          class="plans-btn no-border-radius"
          outlined large
        >
          View Plans
        </v-btn>
      </a>
    </v-app-bar>
  </v-container>
</template>

<script>
export default {
  name: 'Navbar'
}
</script>

<style lang="css" scoped>
.no-border-radius {
  border-radius: 0 !important;
}
a {
  text-decoration: none !important;
}
.plans-btn {
  transition: 0.4s background-color linear;
}
.plans-btn:hover {
  background-color: #272727;
  color: white;
}
</style>
