<template>
  <v-container fluid ma-0 pa-0>
    <img src="../assets/imgs/windowbar.png" class="headerimg">
    <v-parallax :src="require('~/assets/imgs/609.jpg')" class="Headimg">
      <welcome id="regis"/>
    </v-parallax>
    <div style=" background-image: linear-gradient(#001b1d, #00375e);">
      <sponsor/>
      <about id="about"/>
      <v-img width="100%" height="200" :src="require('~/assets/imgs/imgcut3.png')"></v-img>
      <timeline id="date"/>
    </div>
    <v-img width="100%" height="100" :src="require('~/assets/imgs/imgcut1.png')"></v-img>

    <div style=" background-image: linear-gradient( #001b2e, #000c15); ">
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
</style>


<script>
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
  methods: {}
};
</script>
