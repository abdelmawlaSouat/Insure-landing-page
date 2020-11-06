<template>
  <v-footer>
    <!-- Social Medias -->
    <v-row class="offset-md-2 col-md-9">
      <v-col>
        <img
        src="@/assets/logo.svg"
        alt="Insure Logo"
        width="100"
      >
      </v-col>
      <a href="#" v-for="(icon, idx) in socialIcons" :key="idx">
        <v-img
          :src="require(`@/assets/${icon.src}`)"
          :alt="icon.alt"
          class="ml-4"
        ></v-img>
      </a>
    </v-row>
    <!-- Links -->
    <v-row class="offset-md-2 col-md-9">
      <v-col
        class="col-md-3"
        v-for="(item, idx) in links"
        :key="idx"
      >
        <v-list>
          <v-subheader>{{ item.title }}</v-subheader>
          <v-list-item
            v-for="(link, idx) in item.links"
            :key="idx"
          >
            <a href="#">
              {{ link.toUpperCase() }}
            </a>
          </v-list-item>
        </v-list>
      </v-col>
    </v-row>

    <!-- Attribution -->
    <div class="attribution">
      <p>
        Challenge by
        <a href="https://www.frontendmentor.io/challenges/insure-landing-page-uTU68JV8"
          target="_blank"
        >
          Frontend Mentor
        </a>.
        Coded by
        <a href="https://personal-website-opal.vercel.app/"
          target="_blank"
        >
          Abdelmawla Souat
        </a>.
      </p>
    </div>
  </v-footer>
</template>

<script>
export default {
  name: 'Footer',
  data () {
    return {
      socialIcons: [
        { src: 'icon-facebook.svg', alt: 'Facebook' },
        { src: 'icon-twitter.svg', alt: 'Twitter' },
        { src: 'icon-pinterest.svg', alt: 'Pinterest' },
        { src: 'icon-instagram.svg', alt: 'Instagram' }
      ],
      links: [
        {
          title: 'Our company',
          links: [
            'How we work', 'Why Insure?', 'View plans', 'Reviews'
          ]
        },
        {
          title: 'Help me',
          links: [
            'FAQ', 'Terms of use', 'Privacy policy', 'Cookies'
          ]
        },
        {
          title: 'Contact',
          links: ['Sales', 'Support', 'Live chat']
        },
        {
          title: 'Others',
          links: ['Careers', 'Press', 'Licenses']
        }
      ]
    }
  }
}
</script>

<style lang="css" scoped>
a {
  text-decoration: none;
  color: black !important;
}
.v-footer {
  font-family: "Karla" !important;
}
.v-list-item {
  font-size: 13px !important;
}
.attribution {
    font-size: 12px;
    text-align: center;
    width: 100%;
}
.attribution a {
  color: hsl(228, 45%, 44%) !important;
}
</style>
