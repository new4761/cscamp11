<style>
@import url("https://fonts.googleapis.com/css?family=Mitr:300");
@import url("https://use.fontawesome.com/releases/v5.7.2/css/all.css");
</style>

<template  >
  <v-app dark style=" font-family: 'Mitr', sans-serif !important;">


    <v-content>
      <v-container style="font-family: 'Mitr', sans-serif !important;" align-content-center fluid ma-0 pa-0>
        <nuxt v-scroll="checkoffset" style="background-color:#001b1d; font-family: 'Mitr', sans-serif !important;"/>
      </v-container>
    </v-content>
    <v-scale-transition>
      <v-btn v-show="goTopbutton" @click="$vuetify.goTo(0)" fixed dark fab bottom right color="red">
        <v-icon>keyboard_arrow_up</v-icon>
      </v-btn>
    </v-scale-transition>

    <Footer/>
  </v-app>
</template>

<script>
import Footer from "~/components/footer.vue";
import Header from "~/components/header.vue";

export default {
  components: {
    Footer,
    Header
  },

  data() {
    return {
      //windowWidth: 0,
      WindowHeight: 0,
      goTopbutton: false,
      clipped: false,
      drawer: false,
      fixed: false,

      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "CSCAMP-11"
    };
  },
  mounted() {},
  methods: {
    checkoffset() {
      this.WindowHeight = document.documentElement.scrollTop;
      //console.log(document.documentElement.scrollTop);
      if (this.WindowHeight >= 500) {
        this.goTopbutton = true;
      } else this.goTopbutton = false;
    }
  }
};
</script>

<style>
.divcom {
 background-color:rgba(0,0,0,0) !important;
}
</style>
