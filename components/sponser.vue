<template>

  <v-hover>
    <v-img  v-bind:src="imgSrc" contain max-height="200"  min-height="100">
    </v-img>
   
  </v-hover>

</template>
<script>
export default {
  props: ["imgSrc"]
};
</script>
