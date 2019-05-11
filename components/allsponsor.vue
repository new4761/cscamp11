<template>
  <v-layout>
    <v-flex xs12 sm10 offset-sm1 text-xs-center>
      <v-card flat color="rgb(0,0,0,0)" style=" background-color:rgba(0,0,0,0) !important;">
        <v-container grid-list-md fluid>
          <v-layout row wrap>
            <v-flex xs4 sm3 v-for="(campkey,i)  in Headcampsponsor" :key="i">
              <a style=" text-decoration: none;" :href=" campkey.link ">
                <v-card
                  flat
                  color="rgb(0,0,0,0) "
                  style=" background-color:rgba(0,0,0,0) !important;"
                >
                  <v-img
                    transition="fade-transition"
                    :src=" getImgUrl(campkey.src)"
                    contain
                    :alt=" campkey.name"
                    height="200px"
                  ></v-img>
                </v-card>
              </a>
            </v-flex>
          </v-layout>
        </v-container>
      </v-card>
    </v-flex>
  </v-layout>
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
        },  {
          //cscamp
          src: "Emwork",
          name: "Emwork group",
          link: "https://www.emworkgroup.com/th/page/item/index/id/1"
        },
        {
          //cscamp
          src: "Double_A",
          name: "Double A",
          link: "https://www.doubleapaper.com/th/"
        },
          {
          //cscamp
          src: "idea",
          name: "idea A",
          link: "http://www.ideaonpaper.com/th/"
        },
        {
          //cscamp
          src: "iwit",
          name: "iwit",
          link: "http://www.iwit.co.th/"
        },
        {
          //cscamp
          src: "Witty",
          name: "Witty",
          link: "http://www.witty.co.th/home/index.php"
        },
       
       {
          //cscamp
          src: "cs",
          name: "cs",
          link: "https://www.facebook.com/cskmitl/"
        },
        {
          //cscamp
          src: "cscamp",
          name: "cscamp",
          link: "https://cs-camp.net/"
        },
      ]
    };
  },
  methods: {
    getImgUrl(pet) {
      var images = require.context("../assets/sponsor", false, /\.png$/);
      return images("./" + pet + ".png");
    }
  }
};
</script>
<style>
@import "../assets/style/sponser.css"; /* Using a string */
</style>
