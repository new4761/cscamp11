<template>
  <v-container grid-list-sm >
    <v-flex xs12 sm10 offset-sm1 text-xs-center>
       <br>
      <br>
      <div
        style="border-style:solid; border-color:#01ffff; color:#01ffff;"
        class="display-1 thaifont"
      >ภาพกิจกรรม CSCAMP X (10)</div>
       <br>
    <br>
    </v-flex>
   
 <v-layout align-center justify-center  wrap>
      <v-flex xs4 class="text-xs-center" v-for="n in imagesmax" :key="n">
        <p >
          <v-img
            transition="fade-transition"
            :src=" getImgUrl(n)"
           contain  max-height="200px"
          ></v-img>
  
        </p>

        <br>
        <br>
      </v-flex>
    </v-layout>
    <!-- <v-layout align-center justify-center wrap >
    
        <v-flex   class="text-xs-center" sm3 v-for="n in imagesmax" :key="n">
          <v-flex xs3 sm2 v-for=" n in imagesmax " :key="n">
              <v-flex>
                <v-img aspect-ratio="1" :src="getImgUrl(n)" :lazy-src="getImgUrl(n)"></v-img>
              </v-flex>
          </v-flex>-->
<!--     
      <v-img
            transition="fade-transition"
            :src=" getImgUrl(n)"
            width="200px"
            height="200px"

          
          ></v-img>
      
     
        </v-flex>
   
    </v-layout> --> 
  </v-container>
</template>


<script>
export default {
  data() {
    return {
      n: 0,
      imagesmax: 12
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
