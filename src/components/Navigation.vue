<template>
  <v-app-bar
    app
    color="primary"
    dark
  >
  <v-app-bar-nav-icon></v-app-bar-nav-icon>

    <v-spacer></v-spacer>

    <v-col cols="2">
      <v-select v-model="language" :items="languages" label="Language" class="mt-2"></v-select>
    </v-col>

  </v-app-bar>
</template>

<script>
export default {
  name: 'Navigation',

  data () {
    return {
      language: 'ja',
    }
  },

  computed: {
    languages() {
      return [
        { id : 0, text : "日本語"},
        { id : 1, text : "English"}
    ]}
  },
};
</script>