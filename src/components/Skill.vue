<template>

  <v-col class="mb-5" cols="12">
    <h2 class="headline font-weight-bold">
      <v-icon dence>mdi-lightbulb-on</v-icon>
      Skills
    </h2>
    <br>
    <v-row justify="center">
      <v-card v-for="(item, i) in cardItems"
              :key="i"
              class="mx-4 my-6"
              width="320">
        <v-img height="200px"
               width="320px"
               contain
               :src='require("../assets/" + item.im)'></v-img>
        <v-card-text class="text--primary" v-if="languageId">
          {{ item.en }}
        </v-card-text>
        <v-card-text class="text--primary" v-else>
          {{ item.ja }}
        </v-card-text>
      </v-card>
    </v-row>
  </v-col>

</template>

<script>

  export default {
    name: 'Skill',

    props: {
      languageId: {
        type: Number,
        default: 0
      }
    },

    computed: {
      cardItems() {
        return [
          {
            im: 'laravel.png',
            ja: '株式会社ベンドにてCMSのバックエンドを担当した際に使用',
            en: 'The backend of CMS and website in Bend Inc.'
          },
          {
            im: 'vue.png',
            ja: '株式会社ベンドのCMSのフロントエンドで使用。このページもVue.jsを使用している。',
            en: 'The frontend of CMS and website in Bend Inc.Vue.js is also use in this page'
          },
          {
            im: 'Python.jpg',
            ja: '自分が一番使用する言語、画像認識、Djangoなどのフレームワークだけでなく、学業でも使用している。',
            en: 'The mostly used language and also used in school. Numpy, Keras, OpenCV, Django, etc.'
          },
          {
            im: 'git.png',
            ja: 'いつもお世話になっているバージョン管理システム。複数人での開発には欠かせない。',
            en: 'Used for almost all products in charge.'
          },
          {
            im: 'unity.png',
            ja: 'ゲーム会社に就職する予定なので、Unityの勉強もがんばっています。',
            en: 'I will be working for a game company, so I am studying game davelopment.'
          }
        ]
      }
    }
  }

</script>