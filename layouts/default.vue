<style>
@import url("https://fonts.googleapis.com/css?family=Mitr");
</style>

<template >
  <v-app dark>
    <v-system-bar  window white :clipped-left="clipped" fixed app>
      <v-menu class="hidden-md-and-up">
        <v-toolbar-side-icon slot="activator"></v-toolbar-side-icon>
        <v-list>
          <v-list-tile v-for="item in menu" :key="item.icon">
            <v-list-tile-content>
               <v-btn flat @click="$vuetify.goTo(item.target)" >{{ item.title }}</v-btn>
            </v-list-tile-content>
          </v-list-tile>
        </v-list>
      </v-menu>
 
      <v-toolbar-items class="hidden-sm-and-down">
        <div  v-for="item in menu" :key="item.icon">
      <v-btn flat @click="$vuetify.goTo(item.target)" >{{ item.title }}</v-btn>
        </div>
      </v-toolbar-items>

      <v-spacer></v-spacer>
      <v-icon>remove</v-icon>
      <v-icon>check_box_outline_blank</v-icon>
      <v-icon>close</v-icon>
    </v-system-bar>

    <v-content>
      <v-container style="font-family: 'Mitr', sans-serif" align-content-center fluid ma-0 pa-0>
        <nuxt v-scroll="checkoffset" style="background-color:#001b1d;"/>
      </v-container>
    </v-content>
    <v-scale-transition>
      <v-btn v-show="goTopbutton"  @click="$vuetify.goTo(0)" fixed dark fab bottom right color="red">
        <v-icon>keyboard_arrow_up</v-icon>
      </v-btn>
    </v-scale-transition>

    <Footer/>
  </v-app>
</template>

<script>
import Footer from "~/components/footer.vue";
import Header from "~/components/header.vue";

export default {
  components: {
    Footer,
    Header
  },

  data() {
    return {
      //windowWidth: 0,
      WindowHeight: 0,
      goTopbutton: false,
      test: "run",
      clipped: false,
      drawer: false,
      fixed: false,

      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "CSCAMP-11",
      menu: [
        { title: "สมัครค่าย",target:"#regis" },
        { title: "เกี่ยวกับค่าย",target:"#about" },
        { title: "กำหนดการ",target:"#date" },
        { title: "วิธีการเดินทาง",target:"#path"  },
        { title: "ช่องทางการติดต่อ",target:"#contact" }
      ]
    };
  },
  mounted() {},
  methods: {
    checkoffset() {
      this.WindowHeight = document.documentElement.scrollTop;
      //console.log(document.documentElement.scrollTop);
      if (this.WindowHeight >= 500) {
        this.goTopbutton = true;
      } else this.goTopbutton = false;
    }
  }
};
</script>
