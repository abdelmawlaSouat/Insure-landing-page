<template>
  <div class="about-us">

    <!-- Title -->
    <v-row class="offset-md-2">
      <v-col class="offset-1 col-11 offset-md-0">
        <div class="line"></div>
        <h2 class="custom-title text-h3 my-10">We’re different</h2>
      </v-col>
    </v-row>

    <!-- About Insure -->
    <v-row class="offset-md-2 col-md-9 col-12">
      <v-col
        v-for="(item, idx) in items" :key="idx"
        class="offset-1 col-11 offset-md-0 col-md-4"
        align="center"
      >
        <v-card flat>
          <v-img
            :src="require(`@/assets/${item.icon}`)"
            :alt="item.title"
            width="80"
          ></v-img>
          <h3 class="my-4"> {{ item.title }} </h3>
          <p> {{ item.text }} </p>
        </v-card>
      </v-col>
    </v-row>

    <!-- Find Out Div -->
    <v-row
      class="find-out-div py-5 bg-dark-violet offset-md-2 col-md-9"
      align="center"
    >
      <v-col class="offset-md-1 offset-1 col-12 col-md-7">
        <h4 class="custom-title">
          Find out more <br> about how we work
        </h4>
      </v-col>
      <v-col
        class="offset-md-2"
        align="center"
      >
        <a href="#">
          <v-btn class="no-border-radius" outlined large dark>
            HOW WE WORK
          </v-btn>
        </a>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: 'AboutUs',
  data () {
    return {
      items: [
        {
          icon: 'icon-snappy-process.svg',
          title: 'Snappy Process',
          text: `Our application process can be completed in minutes, 
            not hours. Don’t get stuck filling in tedious forms.`
        },
        {
          icon: 'icon-affordable-prices.svg',
          title: 'Affordable Prices',
          text: `We don’t want you worrying about high monthly costs.
            Our prices may be low, but we still offer the best 
            coverage possible.`
        },
        {
          icon: 'icon-people-first.svg',
          title: 'People First',
          text: `Our plans aren’t full of conditions and clauses to
          prevent payouts. We make sure you’re covered when you need
          it.`
        }
      ]
    }
  }
}
</script>

<style lang="css" scoped>
@media only screen and (max-width: 600px) {
  .about-us {
    margin-top: 10vh !important;
    margin-bottom: 10vh !important;
  }
}

.about-us {
  margin-top: 30vh;
  margin-bottom: 20vh;
}
.line {
  border-top: 1px solid black;
  width: 20%;
}
.find-out-div {
  margin-top: 10vh;
  margin-bottom: 10vh;
}
h2 {
  font-size: 3.75rem;
}
h4 {
  color: white;
  font-size: 3rem;
}
p {
  font-size: 16px;
  opacity: 0.7;
}
.pattern-right {
  position: absolute;
  right: 12vh;
  width: 25%;
}
.no-border-radius {
  border-radius: 0 !important;
}
.custom-title {
  font-family: "DMSerif" !important;
  font-weight: 500 !important;
}
.bg-dark-violet {
  background-color: var(--dark-violet) !important;
}
a {
  text-decoration: none !important;
}
</style>
