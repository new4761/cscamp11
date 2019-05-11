<template>
  <v-container grid-list-sm>
    <v-layout align-center justify-center>
      <v-flex xs12>
        <div class="text-xs-center">
          <img
            v-for="(campkey,i)  in Headcampsponsor"
            :key="i"
            @click="select(campkey)"
            transition="fade-transition"
            :src=" getImgUrl(campkey.src)"
            style="max-width:250px; min-width:100px; height:auto ;cursor: pointer;"
            :alt=" campkey.name"
          >
        </div>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
export default {
  data() {
    return {
      Headcampsponsor: [
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
          src: "lactasoy",
          name: "lactasoy",
          link: "https://www.lactasoy.com/th/"
        }
      ]
    };
  },
  methods: {
    select: function(campkey) {
      window.location.href = campkey.link;
    },
    getImgUrl(pet) {
      var images = require.context("../assets/sponsor/big", false, /\.png$/);
      return images("./" + pet + ".png");
    }
  }
};
</script>
<style>
@import "../assets/style/sponser.css"; /* Using a string */
</style>

  