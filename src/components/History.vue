<template>
  <v-container fluid fill-height>
    <v-row>
    <v-spacer></v-spacer>
    <v-col class="mb-5" cols="10" xl="9" justify="center">
      <h2 class="headline font-weight-bold">
        <v-icon dence>mdi-school</v-icon>
        History
      </h2>
      <br>
      <v-timeline :dense="$vuetify.breakpoint.xs || $vuetify.breakpoint.sm">
        <v-timeline-item v-for="(item,i) in timelineItems" :key="i">
          <v-card class="elevation-4">
            <v-card-title v-if="!$vuetify.breakpoint.xs" class="headline indigo--text text--darken-4">
              {{ item.title }}
            </v-card-title>
            <p v-else class="pt-2 mb-0 indigo--text text--darken-4">
              {{ item.title }}
            </p>
            <v-card-text class="grey--text text--darken-2">
              {{ item.text }}
            </v-card-text>
          </v-card>
        </v-timeline-item>
      </v-timeline>
    </v-col>
    <v-spacer></v-spacer>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'History',

  props: {
    languageId: {
      type: Number,
      default: 0,
    }
  },

  computed: {
    timelineItems() {
      const ja = [
        {
          title: '2017年3月',
          text: '東京都立日比谷高等学校を卒業'
        },
        {
          title: '2017年4月',
          text: '東京大学理科二類に入学'
        },
        {
          title: '2017年5月 ~',
          text: '様々な会社でアルバイトとしてプログラミングスキルを磨く'
        },
        {
          title: '2018年4月 ~ 2018年12月',
          text: '大学生プログラミングスクール「Geek Salon」にてiOSアプリとJavascriptを用いたWebアプリの開発を学ぶ'
        },
        {
          title: '2018年9月',
          text: '進学選択の結果、薬学部に所属する'
        },
        {
          title: '2019年9月 ~',
          text: '株式会社ナガセの開発チームとして社内用のWebサービスやツールの開発に携わる'
        },
        {
          title: '2019年9月',
          text: '株式会社Cygamesのサマーインターンに参加しゲーム制作について学ぶ'
        },
        {
          title: '2019年12月 ~',
          text: '株式会社ベンドのエンジニアとしてウェブサイト「資格タイムズ」のCMSの開発を担当。他にもRedashによる売上分析、社内用のLINE botの作成などの幅広い業務をこなしている'
        },
        {
          title: '2020年1月',
          text: '薬学部内の研究室配属における抽選・振り分けアルゴリズム、およびWebアプリを作成'
        },
        {
          title: '2020年4月',
          text: '分析化学研究室に配属'
        },
        {
          title: '2020年6月~',
          text: '卒業研究として、「全自動１細胞時間分解解析プラットフォーム」の開発を始める'
        },
      ]
      const en = [
        {
          title: 'Mar 2017',
          text: 'Graduated from Tokyo Metropolitan Hibiya High School'
        },
        {
          title: 'Apr 2017',
          text: 'Entered the University of Tokyo'
        },
        {
          title: 'May 2017 ~',
          text: 'Participated in internships at several companies and improved programming skills'
        },
        {
          title: 'Apr 2018 ~ Dec 2018',
          text: 'Participated in Geek Salon, a programming school for college students and created iOS application and web service thanks for mentor’s help'
        },
        {
          title: 'Sep 2018',
          text: 'Assigned to Faculty of Pharmaceutical Sciences'
        },
        {
          title: 'Sep 2018 ~',
          text: 'Engaged in the development of internal Web services and tools as the development team of Nagase Inc.'
        },
        {
          title: 'Sep 2019',
          text: 'Participated in summer intern of Cygames Inc. and learn about game production'
        },
        {
          title: 'Dec 2019 ~',
          text: 'Working for Bend Inc. and Developed a content management service for website "Shikaku Times"'
        },
        {
          title: 'Jan 2020',
          text: 'Created a lottery algorithm and a web application for a laboratory assignment in the Faculty of Pharmacy'
        },
        {
          title: 'Apr 2020',
          text: 'Assigned to Analytical Chemistry Lab'
        },
        {
          title: 'Jun 2020 ~',
          text: 'Started a development of "Full-automatic 1-cell time-resolved analysis platform" As a graduation research'
        },
      ]
      return [ ja, en ][this.languageId]
    },

    denseTimeline() {
      return this.$vuetify.breakpoint.xs
    }
  }
}
</script>