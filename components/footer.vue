<template>

  <v-layout row>
     
    <div style="position:-webkit-fixed;
  position:fixed;
   bottom:2.5em;">
      <infinite-slide-bar :barStyle="{ background: 'rgb(253, 253, 253,90)', padding: '5px 0 ' }" duration="20s" >
        <div
          v-for="campkey in campsponsor"
          :key="campkey"
          style="display:inline; padding:30px; widht:400%;"
        >
          <a style=" text-decoration: none;" :href=" campkey.link ">
            <v-avatar size="30">
              <img :src=" getImgUrl(campkey.src)" :alt=" campkey.name">
            </v-avatar>
            <span style="color: #000000;  font-size:1.0vw; padding:10px;">{{ campkey.name }}</span>
          </a>
        </div>
      </infinite-slide-bar>
    </div>
    
    <v-footer fixed style="width:100%;"  >
      <v-flex  xs12>
        <div class="text-xs-center">CSCAMP - 11 &copy; {{ new Date().getFullYear() }}</div>
      </v-flex>
    </v-footer>
  </v-layout>
</template>

  <script>
import InfiniteSlideBar from "vue-infinite-slide-bar";

export default {
  components: {
    InfiniteSlideBar
  },
  data() {
    return {
      campsponsor: [
        {
          //cscamp
          src: "LOGO.png",
          name: "CSCAMP-11 SPONSOR",
          link: "https://www.cs-camp.net/"
        },
        {
          //cscamp
          src: "LOGO.png",
          name: "CSCAMP-11 SPONSOR",
          link: "https://www.cs-camp.net/"
        }
      ]
    };
  },
  methods: {
    getImgUrl(pet) {
      var images = require.context("../assets/imgs", false);
      return images("./" + pet);
    }
  }
};
</script>
  