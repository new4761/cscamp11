<template>
  <v-parallax    class="Headimg " height="auto" contain :src="require('~/assets/imgs/hogwarts.png')">
    <v-container fluid grid-list-sm class=".headimg">
      <v-layout align-center justify-center row fill-height text-xs-left  >
        <v-flex xs6>
          <div>
            <v-img
              floating
              aspect-ratio="1"
              max-height="600"
              transition="scale-transition"
              width="auto"
              min-height="300"
              contain
              :src="require('~/assets/imgs/LOGO.png')"
              position="center right"
             
            ></v-img>
          </div>
        </v-flex>
        <v-flex xs6>
          <div>
            <v-card color="blue-grey" dark tile flat>
              <v-card-text
                justify-center
                align-center
                class="thaifont text-truncate"
                style=" float: right;"
              >
                <h4 class="head " contain>ค่ายฝึกอบรมเชิงปฏิบัติการ 
                  <br>
                  <p style="text-decoration: underline; ">วิทยาการคอมพิวเตอร์ ครั้งที่ 11</p>
                </h4>
                <v-spacer></v-spacer>

                <h6 class="sub">ภาควิชาวิทยาการคอมพิวเตอร์ คณะวิทยาศาสตร์
                  <br>สถาบันเทคโนโลยีพระจอมเกล้าคุณทหารลาดกระบัง
                </h6>
              </v-card-text>
            </v-card>
          </div>
        </v-flex>
      </v-layout>
    </v-container>
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
// :style="'-webkit-clip-path: polygon(48% 36%, 100% 0%, 100% 100%, 0% 100%);'"
</script>
<style>
@import "../assets/style/fontthai.css"; /* Using a string */
.headimg {
  background-image: url(../assets/imgs/headertest.svg);
  background-position: center top;
  background-size: 100% 100%;
}

</style>