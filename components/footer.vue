<template style="background-color:#ffff; ">
  <v-layout row style="background-color:#ffff; ">
    <v-flex xs12>
      <div
        style="position:-webkit-fixed;position:fixed;bottom:2.5em; width:100%; background-color:#ffff;max-height: 30px;  "
      >
        <infinite-slide-bar
          :barStyle="{ background: 'rgb(253, 253, 253,90)', padding: '5px 0 '}"
          duration="20s"
        >
          <div v-for="(campkey,i)  in campsponsor" :key="i" style="display:inline; padding:30px;  ">
            <a style=" text-decoration: none;" :href=" campkey.link ">
              <v-avatar size="20">
                <img :src=" getImgUrl(campkey.src)" :alt=" campkey.name">
              </v-avatar>
              <span style="color: #000000;  font-size:13px; padding:10px;">{{ campkey.name }}</span>
            </a>
          </div>
        </infinite-slide-bar>
      </div>
    </v-flex>
    <v-footer fixed style="width:100%;">
      <v-flex xs12>
        <div
          class="text-xs-center"
        >CSCAMP - 11 &copy; {{ new Date().getFullYear() }}- All Rights Reserved</div>
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
          src: "Refinitiv",
          name: "Refinitiv",
          link: "https://www.refinitiv.com/en"
        },
        {
          //cscamp
          src: "news",
          name: "krobkruakao3",
          link: "http://www.krobkruakao3.org/"
        },
        {
          //cscamp
          src: "borntodev",
          name: "borntodev",
          link: "https://www.borntodev.com/"
        },
          {
          //cscamp
          src: "Krungsri",
          name: "Krungsri",
          link: "https://www.krungsri.com/bank/th/home.html"
        },
  {
          //cscamp
          src: "ican",
          name: "YES I  CAN",
          link: "#"
        },
          {
          //cscamp
          src: "lactasoy",
          name: "lactasoy",
          link: "https://www.lactasoy.com/th/"
        },

        {
          //cscamp
          src: "thaibev",
          name: "thaibev",
          link: "http://www.thaibev.com/"
        },
         {
          //cscamp
          src: "eisa",
          name: "eisa",
          link: "http://www.thaibev.com/"
        },
        {
          //cscamp
          src: "orc",
          name: "ORCSOFT",
          link: "https://orcsoft.co.th/"
        },
      
      ]
    };
  },
  methods: {
    getImgUrl(pet) {
      var images = require.context("../assets/sponsor/", false, /\.png$/);
      return images("./" + pet + ".png");
    }
  }
};
</script>
  