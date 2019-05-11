<template>
  <v-container grid-list-sm fluid>
    <v-flex xs12 sm10 offset-sm1 text-xs-center>
      <br>
      <br>
      <div
        style="border-style:solid; border-color:#01ffff; color:#01ffff;"
        class="display-1 thaifont"
      >กำหนดการ</div>
      <br>
      <br>
    </v-flex>
    <v-layout align-center justify-center  wrap>
      <v-flex sm3 class="text-xs-center" v-for="(campkey,i) in Headcampsponsor" :key="i">
        <p :style="{color:campkey.color,}" class="subheading thaifont">
          <v-img
            transition="fade-transition"
            :src=" getImgu(campkey.src)"
            max-height="200px"
            contain
          ></v-img>
          <br>
          {{campkey.note}}
          เริ่ม {{campkey.DateS}}
          <br>
          หมดเขต {{campkey.DateE}}
        </p>

        <br>
        <br>
      </v-flex>
    </v-layout>
    <v-flex text-xs-center>ติดตามรายละเอียดเพิ่มเติมได้ที่ facebookpage =>
      <v-btn color="indigo" href="https://www.facebook.com/cskmitl.camp">
        <v-icon size="16px" class="pr-2">fab fa-facebook</v-icon>CSCAMP
      </v-btn>
    </v-flex>
  </v-container>
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
          DateS: "11/3/2019",
          DateE: "28/4/2019"
        },
        {
          //cscamp
          src: "anw.png",
          note: "ประกาศผลการคัดเลือก",
          color: "#e4ff00",
          DateS: "11/5/2019",
          DateE: "19/5/2019"
        },
        {
          //cscamp
          src: "vali.png",
          note: "ยืนยันสิทธิ์",
          color: "#ff9c00",
          DateS: "11/5/2019",
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

