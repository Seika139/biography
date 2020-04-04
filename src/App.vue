<template>
  <v-app>
    <navigation/>
    <v-content>
      <v-container>
        <v-row class="text-center">
          <profile/>
          <skill/>
          <history/>
          <contact/>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
  import { Navigation, Profile, Skill, History, Contact } from './components/'

  export default {
    name: 'App',

    components: {
      Navigation,
      Profile,
      Skill,
      History,
      Contact
    },

    data: () => ({
      //
    })
  }
</script>
