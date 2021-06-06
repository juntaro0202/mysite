<template>
  <v-container>
    <v-row justify="center" align="center">
      <h2>じゅんちゃんの活動</h2>
    </v-row>
    <v-row justify="center">
      <v-timeline
        align-top
        :dense="$vuetify.breakpoint.smAndDown"
      >
        <v-timeline-item
          v-for="(item, i) in items"
          :key="i"
          :color="item.color"
          :icon="item.icon"
          :title="item.title"
          :content="item.content"
          :href="item.href"
          fill-dot
        >
          <v-card
            :color="item.color"
          >
            <v-card-title
             class="text-h6">
              <h2 class="text-h4 white--text font-weight-light">
                {{item.title}}
              </h2>
            </v-card-title>
            <v-card-text class="white text--primary">
              <p>{{item.content}}</p>
              <v-btn
                :color="item.color"
                :href="item.href"
                class="mx-0"
                outlined
              >
                詳しく
              </v-btn>
            </v-card-text>
          </v-card>
        </v-timeline-item>
      </v-timeline>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      items: [
        {
          color: 'red',
          icon: 'mdi-youtube',
          title: 'youtube',
          content: 'youtubeにて哲学入門チャンネルを開設しています。主に時事ネタと哲学を絡めた話をしています。',
          href: 'https://www.youtube.com/channel/UCa6oNOr1S251sHs8rile4Rw',
        },
        {
          color: 'blue',
          icon: 'mdi-twitter',
          title: 'twitter',
          content: 'twitterはじめてみました。反陰部論者として日夜ツイートしてます。',
          href: 'https://twitter.com/junchann0202?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor',
        },
        {
          color: 'purple darken-1',
          icon: 'mdi-bee',
          title: '読書会',
          content: '読書会を主催しています。哲学書だけではなく、教養書まで幅広く扱い、気楽に来れる雰囲気のものを目指しています。現在はオンラインのみでの開催です。',
          href: 'http://polis-dokusyokai.com/',
        },
        {
          color: 'green lighten-1',
          icon: 'mdi-book',
          title: '書籍',
          content: 'さくっと著名な哲学書の内容が分かる本を書きました。',
          href: 'https://amzn.to/3bNTCIK',
        },
      ],
    }),
  }
</script>