<template>
  <v-container fluid>
    <v-layout align-center justify-center row text-xs-left>
      <v-flex xs12>
        <div>
          <v-img
            floating
            aspect-ratio="1"
            max-height="500"
            transition="scale-transition"
            width="auto"
            min-height="300"
            contain
            :src="require('~/assets/imgs/LOGO.png')"
            position="center right"
          ></v-img>
        </div>
      </v-flex>
      <v-flex xs12>
        <div>
          <v-card
            flat
            justify-center
            align-center
            class="thaifont"
            style="float: left;text-align:center;   word-wrap: break-word; border-style:solid; border-color:#01ffff; "
            color="rgb(255,255,255,0.3)"
          >
            <v-card-text style="background-color:#01ffff;">
              <span
                class="thaifont"
                style="color:#00073e; font-size:3vw;"
                contain
              >ค่ายฝึกอบรมเชิงปฏิบัติการ
                <br>วิทยาการคอมพิวเตอร์ ครั้งที่ 11
              </span>
            </v-card-text>

            <v-divider style="heigh:20px"></v-divider>
            <v-card-text>
              <h6 style="color:#ffff; font-size:1.8vw;">ภาควิชาวิทยาการคอมพิวเตอร์ คณะวิทยาศาสตร์
                <br>สถาบันเทคโนโลยีพระจอมเกล้าคุณทหารลาดกระบัง
              </h6>
            </v-card-text>
          </v-card>
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
    return {};
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