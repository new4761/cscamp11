<template>
  <v-container fluid ma-0 pa-0>
    <welcome/>
    <sponser/>
    <about/>
    <timeline/>
  <gallery/>

  <contact/>
  <allsponser/>
  </v-container>
</template>

<script>
import welcome from "~/components/welcome.vue";
import sponser from "~/components/sponser.vue";
import about from "~/components/about.vue";
import timeline from "~/components/timeline.vue";
import gallery from "~/components/gallery.vue";

import contact from "~/components/contact.vue";
import allsponser from "~/components/allsponser.vue";
//import Logo from "~/components/Logo.vue";
//import VuetifyLogo from "~/components/VuetifyLogo.vue";

export default {
  components: {
    welcome,sponser,about,timeline,gallery,contact,allsponser
    //  Logo,
    // VuetifyLogo
  },
  methods: {}
};
</script>
