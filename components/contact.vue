<template>
  <v-container justify-center text-xs-center>
    <br>
    <v-layout wrap>
      <v-flex xs10 offset-xs1>
        <v-card
          class="mx-auto"
          color="rgba(255, 255, 255,0)"
          style="padding-left:0.5em; border-style:solid; border-color:#01ffff;"
        >
          <v-card-title>
            <div>
              <div justify-center style="color:#00c6c6; " class="headline thaifont">
                <v-icon style="color:#00c6c6;" large left>call</v-icon>ช่องทางการติดต่อ
              </div>
            </div>
          </v-card-title>

          <v-expansion-panel focusable>
            <v-expansion-panel-content
              v-for="(pathMap,i) in pathMap"
              :key="i"
              :prepend-icon="pathMap.icon"
              style="background-color:rgba(255, 0, 0, 0.0 ); "
            >
              <div style="color:#01ffff;  " slot="header">
                <v-icon style="color:#01ffff;">{{pathMap.icon}}</v-icon>
                {{ pathMap.name }}
              </div>
              <v-card
                v-for=" more in pathMap.more"
                :key="more.text"
                style="background-color:#018989 ;"
              >
                <v-card-text>{{ more.text }}</v-card-text>
              </v-card>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-card>
      </v-flex>
      <v-flex xs12 align-center justify-center>
        <div class="mapouter">
          <div class="gmap_canvas mx-auto">
            <iframe
              width="80%"
              height="300"
              id="gmap_canvas"
              src="https://maps.google.com/maps?q=%E0%B8%84%E0%B8%93%E0%B8%B0%E0%B8%A7%E0%B8%B4%E0%B8%97%E0%B8%A2%E0%B8%B2%E0%B8%A8%E0%B8%B2%E0%B8%AA%E0%B8%95%E0%B8%A3%E0%B9%8C%20%E0%B8%A5%E0%B8%B2%E0%B8%94%E0%B8%81%E0%B8%A3%E0%B8%B0%E0%B8%9A%E0%B8%B1%E0%B8%87&t=&z=11&ie=UTF8&iwloc=&output=embed"
              frameborder="0"
              scrolling="no"
              marginheight="0"
              marginwidth="0"
            ></iframe>
          </div>
        </div>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
export default {
  data() {
    return {
      pathMap: [
        {
          //cscamp

          name: "สถานที่จัดค่าย ",
          more: [
            {
              text:
                "3 ถนน ฉลองกรุง แขวง ลำปลาทิว เขต ลาดกระบัง กรุงเทพมหานคร 10520 "
            }
          ],
          show: false,
          icon: "location_on"
        },
             {
          //cscamp

          name: "Email ",
          more: [
            {
              text:
                "kmitlcscamp@gmail.com"
            }
          ],
          show: false,
          icon: "mail"
        },
        {
          //cscamp

          name: "Phone",
          more: [
            {
              text:
                "พี่อู๋ 090-638-9907"
            }
          ],
          show: false,
          icon: "call"
        }
      ]
    };
  }
};
</script>

 <style>
@import "../assets/style/fontthai.css";
.mapouter {
  padding-top: 3em;
}
.gmap_canvas {
  overflow: hidden;
  background: none !important;
}
</style>