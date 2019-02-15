<template>
  <v-layout>
    <v-flex xs12 sm10 offset-sm1 text-xs-center>
      <v-card flat color="rgb(0,0,0,0)">
        <v-container grid-list-md fluid>
          <v-layout row wrap>
            <v-flex xs4 sm3 v-for="(campkey,i)  in Headcampsponsor" :key="i">
              <a style=" text-decoration: none;" :href=" campkey.link ">
                <v-card flat color="rgb(0,0,0,0)">
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
          src: "cs",
          name: "CSCAMP-11 SPONSOR",
          link: "https://www.cs-camp.net/"
        },
        {
          //cscamp
          src: "cs",
          name: "CSCAMP-11 SPONSOR",
          link: "https://www.cs-camp.net/"
        },
        {
          //cscamp
          src: "cscamp",
          name: "CSCAMP-11 SPONSOR",
          link: "https://www.cs-camp.net/"
        },
        {
          //cscamp
          src: "cscamp",
          name: "CSCAMP-11 SPONSOR",
          link: "https://www.cs-camp.net/"
        },
        {
          //cscamp
          src: "cs",
          name: "CSCAMP-11 SPONSOR",
          link: "https://www.cs-camp.net/"
        },
        {
          //cscamp
          src: "cs",
          name: "CSCAMP-11 SPONSOR",
          link: "https://www.cs-camp.net/"
        },
        {
          //cscamp
          src: "cscamp",
          name: "CSCAMP-11 SPONSOR",
          link: "https://www.cs-camp.net/"
        },
        {
          //cscamp
          src: "cscamp",
          name: "CSCAMP-11 SPONSOR",
          link: "https://www.cs-camp.net/"
        }
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
