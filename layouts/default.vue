<template>
  <v-app dark>
    <v-toolbar :clipped-left="clipped" fixed app>
      <v-toolbar-side-icon @click="drawer = !drawer"/>
      <v-toolbar-title v-text="title"/>
    </v-toolbar>

    <v-content>
    <v-container>
    

        <nuxt  v-scroll="checkoffset"/>
         <br> Window height: {{ oldWindowHeight }}
         </v-container>
    </v-content>
    
    <!-- <v-btn v-show="false" fixed dark fab bottom right color="red" @click="$vuetify.goTo(0) ">
      <v-icon>keyboard_arrow_up</v-icon>
    </v-btn> -->
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
      oldWindowHeight: 0,
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
    mounted() {

  },
  methods: {
    checkoffset() {
     console.log(document.documentElement.scrollTop );
      // this.$refs.target.textContent = this.getWindowHeight;
      // console.log(this.$refs.target.scrollHeight);

      //this.$refs.targe;
    },
    //  getWindowWidth(event) {
    //     this.windowWidth = document.documentElement.clientWidth;
    //   },
  
     
  },
  
};
</script>
