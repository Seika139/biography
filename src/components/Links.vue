<template>
  <v-container fluid>
    <v-row justify="center">
      <v-col cols="12" sm="8">
        <h2 class="headline font-weight-bold">
          <v-icon dence>mdi-link-variant</v-icon>
          Links
        </h2>
        <br>
        <v-card v-for="(item, i) in links" :key="i" class="ma-3 pa-2">
        <v-list-item two-line>
          <v-list-item-content class="text-left">
            <v-list-item-title class="pb-2">
              <a :href="item.href" target="_blank">{{ item.title }}</a>
            </v-list-item-title>
            <v-list-item-subtitle>{{ item.text }}</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Links',

  props: {
    languageId: {
      type: Number,
      default: 0,
    }
  },

  computed: {
    links() {
      const ja = [
        {
          title: '東京大学大学院薬学系研究科 生体分析科学教室 Webページ',
          text: '私が所属する研究室のWebページです',
          href: 'http://www.f.u-tokyo.ac.jp/~funatsu/index.html',
        },
        {
          title: '将来に直結するウェブプログラミング ｜資格Timesの東大生エンジニア鈴木健一',
          text: '勤務先である株式会社ベンドのWantedlyにある私のインタビュー記事です',
          href: 'https://www.wantedly.com/companies/company_7765230/post_articles/223076',
        },
      ]
      const en = [
        {
          title: 'Laboratory of Bioanalytical Chemistry | The University of Tokyo',
          text: 'the web page of my laboratory',
          href: 'http://www.f.u-tokyo.ac.jp/~funatsu/index.html',
        },
        {
          title: 'Bend Inc. Wantedly | My Interview Article',
          text: 'This is my interview article in Wantedly from Bend Inc.',
          href: 'https://www.wantedly.com/companies/company_7765230/post_articles/223076',
        },
      ]
      return [ ja, en ][this.languageId]
    },
  },
}
</script>