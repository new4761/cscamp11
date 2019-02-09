<template>
  <v-layout>
    <v-flex xs12 sm10 offset-sm1 text-xs-center>
      <v-card flat>
        <v-container grid-list-md fluid>
          <v-layout row wrap>
            <v-flex xs3 v-for="campkey in Headcampsponsor" :key="campkey">
              <a style=" text-decoration: none;" :href=" campkey.link ">
                <v-card flat>
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
          src: "LOGO.png",
          name: "CSCAMP-11 SPONSOR",
          link: "https://www.cs-camp.net/"
        },
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
<style>
@import "../assets/style/sponser.css"; /* Using a string */
</style>

