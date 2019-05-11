<template style="background-color:#000;">
  <v-system-bar window white  fixed app >
     <v-menu class="hidden-md-and-up">

        <v-toolbar-side-icon slot="activator"></v-toolbar-side-icon>
        <br>
          <v-list pl-1>
        <v-list-tile v-for="(menu, i) in menu" :key="i" dark @click="$vuetify.goTo(menu.target)">
          <v-list-tile-title >{{ menu.title }}</v-list-tile-title>
        </v-list-tile>
      </v-list>
      </v-menu>
    <div class="hidden-sm-and-down">
    <v-menu bottom transition="slide-y-transition">
      <v-btn
        transition="slide-y-transition"
        open-on-click
        close-on-content-click
        flat
        slot="activator"
      >
        <v-avatar :size="30" tile>
          <v-img aspect-ratio="1" class="hbutton" :src="require('~/assets/header/h_win.png')"></v-img>
        </v-avatar>
      </v-btn>
      <br>
      <v-list pl-1>
        <v-list-tile v-for="(menu, i) in menu" :key="i" dark @click="$vuetify.goTo(menu.target)">
          <v-list-tile-title >{{ menu.title }}</v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-menu>

    <!-- <v-btn flat>
      <v-avatar :size="30">
        <v-img class="hbutton" :src="require('~/assets/header/h_fol.png')"></v-img>
      </v-avatar>
    </v-btn>-->
    <v-btn flat href="https://www.facebook.com/cskmitl/">
      <v-avatar :size="30" tile>
        <v-img class="hbutton" :src="require('~/assets/header/h_cs.png')"></v-img>
      </v-avatar>
    </v-btn>
    <v-btn flat href="https://www.reg.kmitl.ac.th">
      <v-avatar :size="30" tile>
        <v-img class="hbutton" :src="require('~/assets/header/h_km.png')"></v-img>
      </v-avatar>
    </v-btn>
    <v-btn flat href="https://cs-camp.net">
      <v-avatar :size="30" tile>
        <v-img class="hbutton" :src="require('~/assets/header/h_camp.png')"></v-img>
      </v-avatar>
    </v-btn>

      </div>
    <v-spacer></v-spacer>
     

  
  </v-system-bar>
  
</template>
<script>
export default {
  data() {
    return {
      date:
        new Date().getFullYear() +
        "/" +
        (new Date().getMonth() + 1) +
        "/" +
        new Date().getDate(),
      time: new Date().getHours() + ":" + new Date().getMinutes(),
      window: [
        { src: "h_win" },
        { src: "h_fol" },
        { src: "h_cs" },
        { src: "h_km" },
        { src: "h_camp" }
      ],
      menu: [
        { title: "สมัครค่าย", target: "#regis" },
        { title: "เกี่ยวกับค่าย", target: "#about" },
        { title: "กำหนดการ", target: "#date" },
        { title: "วิธีการเดินทาง", target: "#path" },
        { title: "ช่องทางการติดต่อ", target: "#contact" }
      ]
    };
  },
  methods: {
    getImgUrl(pet) {
      var images = require.context("../assets/header/", false, /\.png$/);
      return images("./" + pet + ".png");
    }
  }
};
</script>

