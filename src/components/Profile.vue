<template>
  <v-row>
  <v-col cols="12">
    <v-avatar class="my-3" size="200">
      <img :src="require('../assets/icon.jpg')">
    </v-avatar>
  </v-col>

  <v-col class="mb-4">
    <h1 class="display-2 font-weight-bold mb-3">
      Kenichi Suzuki
    </h1>

    <p class="subheading font-weight-regular">
      For help and collaboration with other Vuetify developers,
      <br>please join our online
      <a href="https://community.vuetifyjs.com" target="_blank">Discord Community</a>
    </p>
  </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'Profile',

  computed: {
    timelineItems() {
      return [
        { title: "First", text: "English", date: "2015"},
        { title: "First", text: "English", date: "2015"},
        { title: "First", text: "English", date: "2015"},
      ]
    }
  }
}
</script>