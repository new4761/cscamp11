<template>
  <v-app dark>
    <v-toolbar :clipped-left="clipped" fixed app>
      <v-avatar size="60">
        <img src="../assets/LOGO.png" alt="avatar">
      </v-avatar>
        <v-toolbar-title v-text="title"/>
      <v-toolbar-side-icon @click="drawer = !drawer"/>
    </v-toolbar>

    <v-content>
      <v-container grid-list-md fluid ma-0 pa-0>
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
