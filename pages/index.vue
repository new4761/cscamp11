<template>
  <v-container fluid ma-0 pa-0>
    <welcome />
    <sponsor/>
    <about/>
    <timeline/>
  <gallery/>

  <contact/>
  <allsponsor/>
  </v-container>
</template>

<script>
import welcome from "~/components/welcome.vue";
import sponsor from "~/components/sponsor.vue";
import about from "~/components/about.vue";
import timeline from "~/components/timeline.vue";
import gallery from "~/components/gallery.vue";

import contact from "~/components/contact.vue";
import allsponsor from "~/components/allsponsor.vue";
//import Logo from "~/components/Logo.vue";
//import VuetifyLogo from "~/components/VuetifyLogo.vue";

export default {
  components: {
    welcome,sponsor,about,timeline,gallery,contact,allsponsor
    //  Logo,
    // VuetifyLogo
  },
  methods: {}
};
</script>
