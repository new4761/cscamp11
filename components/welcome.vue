<template>
  <v-parallax height="300" src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg">
    <v-layout pt-3 align-start justify-space-around row fill-height text-xs-center>
      <v-flex pa-1>
        <sponser v-bind:imgSrc="require('~/assets/imgs/temp_spon.png')"/>
        <sponser v-bind:imgSrc="require('~/assets/imgs/temp_spon.png')"/>
        <sponser v-bind:imgSrc="require('~/assets/imgs/temp_spon.png')"/>
      </v-flex>
      <v-spacer></v-spacer>
      <v-flex pa-1>
        <v-scale-transition>
          <v-img :src="require('~/assets/LOGO.png')"></v-img>
        </v-scale-transition>
      </v-flex>
      <v-spacer></v-spacer>
      <v-flex pa-1>
        <sponser v-bind:imgSrc="require('~/assets/imgs/temp_spon.png')"/>
        <sponser v-bind:imgSrc="require('~/assets/imgs/temp_spon.png')"/>
        <sponser v-bind:imgSrc="require('~/assets/imgs/temp_spon.png')"/>
      </v-flex>
    </v-layout>
  </v-parallax>
</template>

<script>
import sponser from "~/components/sponser.vue";
export default {
  components: {
    sponser
  },

  data() {
    return {};
  },
  mounted() {},
  methods: {}
};
</script>