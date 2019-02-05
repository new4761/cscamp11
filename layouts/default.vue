<template>
  <v-app dark>
    <v-toolbar :clipped-left="clipped" fixed app>
      <v-toolbar-side-icon @click="drawer = !drawer"/>
      <v-toolbar-title v-text="title"/>
    </v-toolbar>

    <v-content>
    
     <Heaer/>
        <nuxt  v-scroll="checkoffset"/>
 
    </v-content>
    <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
      <v-list>
        <v-list-tile @click.native="right = !right">
          <v-list-tile-action>
            <v-icon light>compare_arrows</v-icon>
          </v-list-tile-action>
          <v-list-tile-title>Switch drawer (click me)</v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-btn v-show="false" fixed dark fab bottom right color="red" @click="$vuetify.goTo(0) ">
      <v-icon>keyboard_arrow_up</v-icon>
    </v-btn>
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
      test: "run",
      clipped: false,
      drawer: false,
      fixed: false,

      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js"
    };
  },
  methods: {
    checkoffset() {
      console.log(this.$refs.target.scrollTop);
      this.$refs.target.textContent = this.$refs.target.scrollTop;
      // console.log(this.$refs.target.scrollHeight);

      //this.$refs.targe;
    }
  }
};
</script>
