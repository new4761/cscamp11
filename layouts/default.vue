<style>
@import url('https://fonts.googleapis.com/css?family=Mitr');
</style>

<template>
  <v-app dark>
     <v-system-bar   scroll-off-screen window white  :clipped-left="clipped" fixed app> 
      
      <v-spacer></v-spacer>
      <v-icon>remove</v-icon>
      <v-icon>check_box_outline_blank</v-icon>
      <v-icon>close</v-icon>
    </v-system-bar>
    <v-toolbar  white :clipped-left="clipped" fixed app>
      <v-avatar size="60">
        <img src="../assets/imgs/LOGO.png" alt="cscamp">
      </v-avatar>
      <v-toolbar-title v-text="title"/>
      <v-toolbar-side-icon @click="drawer = !drawer"/>
    </v-toolbar>

    <v-content>
      <v-container style="font-family: 'Mitr', sans-serif" align-content-center fluid ma-0 pa-0>
        <nuxt v-scroll="checkoffset"/>
      </v-container>
    </v-content>
    <v-scale-transition>
      <v-btn v-show="goTopbutton" fixed dark fab bottom right color="red" @click="$vuetify.goTo(0)">
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
      test: "run",
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
