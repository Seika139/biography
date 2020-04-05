<template>
  <v-app>
    <navigation :language-id="languageId" @change="update($event)"/>
    <v-content>
      <v-container>
        <v-row class="text-center">
          <profile :language-id="languageId"/>
          <skill/>
          <history :language-id="languageId"/>
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
      languageId: 0,
    }),

    methods: {
      update(id) {
        this.languageId = id
      },
    },
  }
</script>
