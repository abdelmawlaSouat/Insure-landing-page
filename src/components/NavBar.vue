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
      <div v-if="$vuetify.breakpoint.smAndUp">
        <a
          href="#"
          v-for="(e, i) in 3"
          :key="i"
        >
          <v-btn class="mr-2" text large>
            {{ menuItems[i] }}
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
      </div>

      <div v-else>
        <v-img
          src="@/assets/icon-hamburger.svg"
          alt="Hamburger Menu"
          @click.stop="openMenu = !openMenu"
        ></v-img>
      </div>
    </v-app-bar>

    <!-- Side Menu on mobile -->
    <v-navigation-drawer
          v-model="openMenu"
          absolute
        >
        <v-list>
          <v-list-item-group>
            <v-list-item
              v-for="(item, idx) in menuItems"
              :key="idx"
            >
              <v-list-item-title>
                <a href="#">
                  {{ item }}
                </a>
              </v-list-item-title>
            </v-list-item>
          </v-list-item-group>
        </v-list>
    </v-navigation-drawer>
  </v-container>
</template>

<script>
export default {
  name: 'Navbar',
  data: () => ({
    openMenu: false,
    menuItems: ['How We work', 'Blog', 'Account', 'View Plans']
  })
}
</script>

<style lang="css" scoped>
.no-border-radius {
  border-radius: 0 !important;
}
a {
  text-decoration: none !important;
  color: black !important;
}
.plans-btn {
  transition: 0.4s background-color linear;
}
.plans-btn:hover {
  background-color: #272727;
  color: white;
}
</style>
