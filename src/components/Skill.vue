<template>
<v-col class="mb-5" cols="12">
  <h2 class="headline font-weight-bold mb-3">
    <v-icon dence>mdi-lightbulb-on</v-icon>
    Skills
  </h2>

  <v-row justify="center">
    <a v-for="(link, i) in importantLinks"
       :key="i"
       :href="link.href"
       class="subheading mx-3"
       target="_blank">
          {{ link.text }}
        </a>
  </v-row>
</v-col>
</template>

<script>
export default {
  name: 'Skill',

  data: () => ({
    importantLinks: [
      {
        text: 'Documentation',
        href: 'https://vuetifyjs.com'
      },
      {
        text: 'Chat',
        href: 'https://community.vuetifyjs.com'
      },
      {
        text: 'Made with Vuetify',
        href: 'https://madewithvuejs.com/vuetify'
      },
      {
        text: 'Twitter',
        href: 'https://twitter.com/vuetifyjs'
      },
      {
        text: 'Articles',
        href: 'https://medium.com/vuetify'
      }
    ]
  })
}
</script>