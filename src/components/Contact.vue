<template>

  <v-col class="mb-5" cols="12">
    <h2 class="headline font-weight-bold">
      <v-icon dence>mdi-email</v-icon>
      Contact
    </h2>
    <br>
    <v-row justify="center">
      <v-col v-for="(item, i) in links" :key="i" cols="12" sm="4" lg="3" xl="2">
        <v-icon class="mx-1">{{ item.icon }}</v-icon>
        <a v-if="item.href" class="subheading mx-3" target="_blank" :href="item.href">{{ item.text }}</a>
        <span v-else>{{ item.text }}</span>
      </v-col>
    </v-row>
  </v-col>

</template>

<script>

  export default {
    name: 'Contact',

    data: () => ({
      links: [
        {
          icon: 'mdi-email',
          text: 'tcoanzu@gmail.com'
        },
        {
          icon: 'mdi-github',
          text: 'Github',
          href: 'https://github.com/Seika139'
        },
        {
          icon: 'mdi-magnify',
          text: 'Qiita',
          href: 'https://qiita.com/Seika139'
        }
      ]
    })
  }

</script>