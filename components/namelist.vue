<template>
  <v-layout justify-center align-center row wrap>
    <v-flex xs12 sm10 text-xs-center>
      <v-card
        flat
        justify-center
        align-center
        class="thaifont"
        style="text-align:center;   word-wrap: break-word; border-style:solid;  "
        color="rgb(255,255,255,0.0)"
      >
        <v-card-text style>
          <h1 class="thaifont" style="color:#01ffff;" contain>
            ประกาศรายชื่อผู้ได้รับคัดเลือก
            <small class="font-weight-thin"></small>
          </h1>
        </v-card-text>
      </v-card>
      <v-layout justify-space-between row wrap>
        <v-flex xs4 v-for="(run,i)  in info" :key="i">
          <v-btn
            max-width="200px"
            class="thaifont"
            outline
            v-if="run[2]==1"
            color="green accent-3"
            style="min-width:300px;"
          >{{run[0]}} {{run[1]}}</v-btn>
          
          <v-btn
            max-width="200px"
            class="thaifont"
            outline
           v-else
            color="amber lighten-1"
            style="min-width:300px;"
          >{{run[0]}} {{run[1]}}</v-btn>
        </v-flex>
      </v-layout>
    </v-flex>

    <br>
  </v-layout>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      info: null
    };
  },
  mounted() {
    axios
      .get(
        "https://sheets.googleapis.com/v4/spreadsheets/1QylCCbv2thJdrERtHCkAexT6UQKqWF6ZoFwfiTNu_ag/values/list!A1:D1000?key=AIzaSyBFD5yNQVy4MqdnGjd4Bz2oRDZmSAD2HUM"
      )
      .then(response => (this.info = response.data.values));
  }
};
</script>
