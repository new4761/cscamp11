<template>
  <v-container justify-center text-xs-center>
    <v-flex xs10 offset-xs1>
      <div
        style="border-style:solid; border-color:#01ffff; color:#01ffff;"
        class="display-1 thaifont"
      >ภาพกิจกรรม CSCAMP X (10)</div>
    </v-flex>
    <br>
    <br>
    <v-spacer></v-spacer>
    <v-flex  flat xs10 offset-xs1>
      <v-carousel flat  hide-delimiters hide-controls>
        <v-carousel-item   v-for=" n in imagesmax " :key="n" :src="getImgUrl(n)"></v-carousel-item>
      </v-carousel>
    </v-flex>
  </v-container>
</template>


<script>
export default {
  data() {
    return {
      n: 0,
      imagesmax: 10
    };
  },
  methods: {
    getImgUrl(pet) {
      var images = require.context("../assets/gallery", false, /\.jpg$/);
      return images("./" + pet + ".jpg");
    }
  }
};
</script>