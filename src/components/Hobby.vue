<template>
  <v-container fluid>
    <v-row justify="center">
      <v-col cols="12">
        <h2 class="headline font-weight-bold">
          <v-icon dence>mdi-gamepad-variant</v-icon>
          Hobby
        </h2>
        <br>
        <v-row justify="center">
          <v-card  v-for="(item,i) in cardItems" :key="i" class="mx-4 my-6" width="320px">
            <v-img  class="white--text" :src="require('../assets/hobby/' + item.img)" height="200px">
              <v-card-title class="font-weight-black">{{ item.title }}</v-card-title>
            </v-img>
            <v-card-text class="text--primary">
              {{ item.text }}
            </v-card-text>
          </v-card>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Hobby',

  props: {
    languageId: {
      type: Number,
      default: 0,
    }
  },

  computed: {
    cardItems() {
      const ja = [
        {
          title: 'サッカー',
          text: '中高時代はサッカー部に所属していました。サッカー観戦も好きです',
          img: 'soccer.jpg',
        },
        {
          title: 'ゲーム',
          text: 'スマホゲームだけでなくPS4やNintendo Switchのゲームなど幅広くプレイしています',
          img: 'game.jpg',
        },
        {
          title: '旅行',
          text: '友達と遠いところに出かけるのが好きで、車で日本中を旅しました',
          img: 'wakayama.jpg',
        },
      ]
      const en = [
        {
          title: 'foot ball',
          text: 'I was on the soccer team in middle and high school. In addition to playing, I love to watch soccer.',
          img: 'soccer.jpg',
        },
        {
          title: 'game',
          text: 'I love playing games. I play not only in smartphones but also in PS4 and Nintendo Switch.',
          img: 'game.jpg',
        },
        {
          title: 'traveling',
          text: 'I like to go to faraway places with my friends, and we have traveled all over Japan by car.',
          img: 'wakayama.jpg',
        },
      ]
      return [ ja, en ][this.languageId]
    }
  },
}
</script>