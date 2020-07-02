<template>
  <v-app-bar
    app
    color="black"
    :hide-on-scroll="false"
    height="70px"
  >
    <v-toolbar-title
      class="font-weight-black headline"
      @click="$vuetify.goTo('#hero')"
    >
      <span class="blue-grey--text text--lighten-3">TINNULONG FOUNDATION</span>
    </v-toolbar-title>

    <v-btn
      text
      class="blue-grey--text text--lighten-2"
      @click="$vuetify.goTo('#hero')"
    >
      Home
    </v-btn>
    <v-btn
      text
      class="blue-grey--text text--lighten-2"
      @click="$vuetify.goTo('#features')"
    >
      Get Involved
    </v-btn>
    <v-btn
      text
      class="blue-grey--text text--lighten-2"
      @click="$vuetify.goTo('#about-us')"
    >
      About
    </v-btn>
    <v-btn
      text
      class="blue-grey--text text--lighten-2"
      @click="$vuetify.goTo('#contact')"
    >
      Contact Us
    </v-btn>

    <v-spacer />

    <v-btn color="orange">
      Donate Now!
    </v-btn>
  </v-app-bar>
</template>

<script>
export default {

}
</script>

<style>

</style>
