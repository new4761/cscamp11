<template>

  
    <v-container fluid grid-list-sm class="headimg" >
      <v-layout>
        <v-flex xs5 >
          <v-img  
            floating
            aspect-ratio="1"
            max-height="400"
            transition="scale-transition"
            width="auto"
            min-height="300"
            contain
            :src="require('~/assets/imgs/LOGO.png')"
            position="center center"
          ></v-img>

        </v-flex>
<v-parallax height="auto" contain :src="require('~/assets/imgs/hogwarts.png')">
        <v-flex xs5 xs12 >
  

          <v-card-text
            justify-center
            align-center
            class="font-weight-black font-family: 'Mitr', sans-serif"
            style="font-size:1.3em;"
          >
            <h4>ค่ายฝึกอบรมเชิงปฏิบัติการ
              <br>วิทยาการคอมพิวเตอร์ ครั้งที่ 11
            </h4>
           
            <h6>ภาควิชาวิทยาการคอมพิวเตอร์ คณะวิทยาศาสตร์
              <br>สถาบันเทคโนโลยีพระจอมเกล้าคุณทหารลาดกระบัง
            </h6>
          </v-card-text>
 
        </v-flex>
          </v-parallax >
      </v-layout>
    </v-container>
 
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
.headimg {
  background-image: url(../assets/imgs/headertest.svg);
    background-position: center top;
    background-size: 100% 100%;
}
</style>