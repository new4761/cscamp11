<template>
  <v-app dark>
    <v-toolbar :clipped-left="clipped" fixed app>
      <v-toolbar-side-icon @click="drawer = !drawer"/>
      <v-toolbar-title v-text="title"/>
    </v-toolbar>
    <v-content>
      <v-container>
        <nuxt/>
      </v-container>
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
    <v-btn fixed dark fab bottom right color="red" @click="$vuetify.goTo(0)">
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
    Footer
  },

  data() {
    return {
      offsetCurren: 0,
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
    onScroll(e) {
      console.log(e.target.offsetCurren);
      // this.offsetCurren = e.target.offsetCurren
    }
  }
};
</script>
