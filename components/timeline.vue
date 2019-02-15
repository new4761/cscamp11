<template>
  <v-layout>
    <v-flex xs12 sm10 offset-sm1 text-xs-center>
      <br>
      <br>
      <div
        style="border-style:solid; border-color:#01ffff; color:#01ffff;"
        class="display-1 thaifont"
      >กำหนดการ</div>
      <br>
      <br>
      <v-card flat color="rgba(255, 255, 255,0)">
        <v-container grid-list-md fluid>
          <v-layout row wrap>
            <v-flex xs3 sm3 v-for="(campkey,i) in Headcampsponsor" :key="i" wrap>
              <v-card flat color="rgba(0, 0, 0, 0.0)">
                <br>
                <v-img
                  transition="fade-transition"
                  :src=" getImgu(campkey.src)"
                  contain
                  height="10vw"
                ></v-img>
                <br>
                <div :style="{color:campkey.color,}" class="subheading thaifont">
                  <p>{{campkey.note}}</p>
                  เริ่ม {{campkey.DateS}}
                  <br>
                  หมดเขต {{campkey.DateE}}
                </div>
              </v-card>
            </v-flex>
            <br>
            <br>
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
          src: "regis.png",
          note: "ประกาศรับสมัคร",
          color: "#00ff00",
          DateS: "18/2/2019",
          DateE: "28/4/2019"
        },
        {
          //cscamp
          src: "anw.png",
          note: "ประกาศผลการคัดเลือก",
          color: "#e4ff00",
          DateS: "13/5/2019",
          DateE: "19/5/2019"
        },
        {
          //cscamp
          src: "vali.png",
          note: "ยืนยันสิทธิ์",
          color: "#ff9c00",
          DateS: "13/5/2019",
          DateE: "19/5/2019"
        },
        {
          //cscamp
          src: "come.png",
          note: "เดินทางสู่ CSCAMP",
          color: "#ff1e00",
          DateS: "31/5/2019",
          DateE: "2/6/2019"
        }
      ]
    };
  },
  methods: {
    getImgu(pet) {
      var images = require.context("../assets/timeline", false);
      return images("./" + pet);
    }
  }
};
</script>
<style>
@import "../assets/style/sponser.css"; /* Using a string */
</style>

