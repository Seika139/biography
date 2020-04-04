<template>

  <v-container>
    <v-row class="text-center">
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

      <history/>
      <skill/>


      <v-col class="mb-5" cols="12">
        <h2 class="headline font-weight-bold mb-3">
          <v-icon dence>mdi-email</v-icon>
          Contact
        </h2>

        <v-row justify="center">
          <a v-for="(eco, i) in ecosystem"
             :key="i"
             :href="eco.href"
             class="subheading mx-3"
             target="_blank">
                {{ eco.text }}
              </a>
        </v-row>
      </v-col>
    </v-row>
  </v-container>

</template>

<script>

  import History from './History'
  import Skill from './Skill'
  export default {
    name: 'Body',

    components: {
      History,
      Skill,
    },

    data: () => ({
      ecosystem: [
        {
          text: 'vuetify-loader',
          href: 'https://github.com/vuetifyjs/vuetify-loader'
        },
        {
          text: 'github',
          href: 'https://github.com/vuetifyjs/vuetify'
        },
        {
          text: 'awesome-vuetify',
          href: 'https://github.com/vuetifyjs/awesome-vuetify'
        }
      ],
    })
  }

</script>
