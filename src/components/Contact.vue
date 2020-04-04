<template>

  <v-row>
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

</template>

<script>

  export default {
    name: 'Contact',

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
      ]
    })
  }

</script>