<template>
  <v-container grid-list-md fluid>
    <v-layout align-center justify-center >
      <v-flex xs12>
        <div>
          <v-img
            floating
            aspect-ratio="1"
            max-height="500"
            transition="scale-transition"
            width="auto"
            min-height="200"
            contain
            :src="require('~/assets/imgs/LOGO.png')"
            position="center center"
          ></v-img>
        </div>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import sponsor from "~/components/sponsor.vue";
export default {
  components: {
    sponsor
  },

  data() {
    return {
      dialog: false,
      opa: 1,
      opa1: 2
    };
  },
  mounted() {},
  methods: {}
};
// :style="'-webkit-clip-path: polygon(48% 36%, 100% 0%, 100% 100%, 0% 100%);'"
</script>
<style>
@import "../assets/style/fontthai.css";
.headerimg {
  width: 100%;
  height: auto;
}
</style>