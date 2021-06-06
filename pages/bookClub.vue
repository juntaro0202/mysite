<template>
  <v-container>
    <h2>読書会</h2>
    <ul>
      <li>このような本を使って読書会をしています。</li>
      <li>ご興味があれば以下のサイトを覗いてみてください。</li>
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
              height="200px"
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
        { title: '読書会１', src: 'あ.png', flex: 4 },
        { title: '読書会１', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', flex: 4 },
        { title: '読書会１', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', flex: 4 },
        { title: '読書会２', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', flex: 6 },
        { title: '読書会３', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 6 },
        { title: '読書会３', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 4 },
        { title: '読書会３', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 4 },
        { title: '読書会３', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 4 },
      ],
    }),
  }
</script>

<style scoped>
ul {
  list-style: none;
}
</style>