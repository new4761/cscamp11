<template>
  <v-container fluid ma-0 pa-0>
    <Headbar/>

    <!-- <img src="../assets/imgs/windowbar.png" class="headerimg"> -->
    <v-parallax :src="require('~/assets/imgs/609.jpg')" class="Headimg">
      <welcome/>
    </v-parallax>

    <div style=" background-image: linear-gradient(#001b1d, #00375e);">
      <v-img width="100%" height="100" :src="require('~/assets/imgs/imgcut4.png')"></v-img>
      <regis id="regis"/>
      <dia></dia>
       
      <sponsor/>
<namelist/>
      <about id="about"/>
      <v-img width="100%" height="200" :src="require('~/assets/imgs/imgcut3.png')"></v-img>

      <timeline id="date"/>
    </div>
    <v-img width="100%" height="100" :src="require('~/assets/imgs/imgcut1.png')"></v-img>

    <div style=" background-image: linear-gradient( #001b2e, #002948); ">
      <br>
      <br>
      <gallery/>
      <pathall id="path"/>
      <contact id="contact"/>
      <allsponsor style=" padding-bottom: 100px;"/>
    </div>
  </v-container>
</template>

<style>
@import url("https://fonts.googleapis.com/css?family=Mitr:300");
@import url("https://use.fontawesome.com/releases/v5.7.2/css/all.css");
</style>


<script>
import namelist from "~/components/namelist.vue";
import dia from "~/components/dia.vue";
import regis from "~/components/regis.vue";
import Headbar from "~/components/header.vue";
import welcome from "~/components/welcome.vue";
import sponsor from "~/components/sponsor.vue";
import about from "~/components/about.vue";
import timeline from "~/components/timeline.vue";
import gallery from "~/components/gallery.vue";
import pathall from "~/components/pathall.vue";
import contact from "~/components/contact.vue";
import allsponsor from "~/components/allsponsor.vue";
//import Logo from "~/components/Logo.vue";
//import VuetifyLogo from "~/components/VuetifyLogo.vue";

export default {
  components: {
    namelist,
    dia,
    regis,
    Headbar,
    welcome,
    sponsor,
    about,
    timeline,
    gallery,
    contact,
    allsponsor,
    pathall
    //  Logo,
    // VuetifyLogo
  },
  methods: {},
  data() {
    return {
      dialog: false
    };
  }
};
</script>
