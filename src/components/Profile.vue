<template>
  <v-container fluid>
    <v-row justify="center">
      <v-col cols="12">
        <v-avatar class="my-3" size="200">
          <img :src="require('../assets/icon.jpg')">
        </v-avatar>
      </v-col>

      <v-col class="mb-4" cols="10">
        <h1 class="display-2 font-weight-bold mb-3">
          {{ nameText }}
        </h1>

        <p class="subheading font-weight-regular">
          {{ profileText }}
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Profile',

  props: {
    languageId: {
      type: Number,
      default: 0,
    }
  },

  computed: {
    nameText() {
      const ja = '鈴木 健一'
      const en = 'Kenichi Suzuki'
      return [ ja, en ][this.languageId]
    },

    profileText() {
      const ja = '東京大学薬学部4年 / ITエンジニア '
      const en = 'The University of Tokyo Faculty of Pharmacy 4th grade / IT engineer'
      return [ ja, en ][this.languageId]
    },
  },
}
</script>