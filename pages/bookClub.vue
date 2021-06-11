<template>
  <v-container>
    <h2>読書会</h2>
    <ul>
      <li>読書会では様々な本を扱っています。</li>
      <li>下の紫ボタンをぽちっとすると読書会のサイトに飛べます。</li>
    </ul>
    <v-btn
      color="purple"
      class="ma-2 white--text"
      href="http://polis-dokusyokai.com/"
    >
      policeサイト
      <v-icon
        right
      >
        mdi-book
      </v-icon>
    </v-btn>
  <v-card
    class="mx-auto"
    
  >
    <v-container fluid>
      <v-row dense>
        <v-col
          v-for="card in cards"
          :key="card.title"
          :cols="card.flex"
        >
          <v-card>
            <v-img
              :src="card.src"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              height="400px"
            >
              <v-card-title v-text="card.title"></v-card-title>
            </v-img>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      cards: [
        { title: 'レーニン著　　　　　　　　　　『帝国主義論』', src: 'レーニン.jpeg', flex: 4 },
        { title: '塩野七生著　　　　　　　　　　『ローマ人の物語』', src: 'ローマは.jpeg', flex: 4 },
        { title: 'フリードリヒ・ハイエク著　　　『貨幣発行自由化論』', src: '貨幣発行.jpeg', flex: 4 },
        { title: '近内悠太著　　　　　　　　　　　　　　　　　　　『世界は贈与でできている　資本主義の「すきま」を埋める倫理学』', src: '世界は.jpeg', flex: 6 },
        { title: 'ジェイミー・バートレット著　　　　　　　　　　　『操られる民主主義』', src: '操られる民主主義.jpeg', flex: 6 },
      ],
    }),
  }
</script>

<style scoped>
ul {
  list-style: none;
}
</style>