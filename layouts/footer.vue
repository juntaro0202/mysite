<template>
  <v-footer
    color="indigo lighten-1"
    padless
  >
    <v-row
      justify="center"
      no-gutters
    >
      <v-btn
        v-for="(item, i) in items"
        :key="i"
        :title="item.title"
        :to="item.to"
        color="white"
        text
        rounded
        class="my-2"
      >
        {{ item.title }}
      </v-btn>
      <v-col
        class="indigo darken-4 text-center white--text"
        cols="12"
      >
        <p>{{ new Date().getFullYear() }} — ©︎じゅんちゃんのサイト</p>
      </v-col>
    </v-row>
  </v-footer>
</template>

<script>
  export default {
    data: () => ({
      items: [
        {
          title: 'じゅんちゃんとは？',
          to: '/'
        },
        {
        title: 'じゅんちゃんの活動',
          to: '/works',
        },
        {
        title: '発信中(youtubeなど)',
          to: '/youtube',
        },
        {
        title: '読書会',
          to: '/bookClub',
        },
        {
        title: 'お問い合わせ',
          to: '/contact',
        },
      ],
    }),
  }
</script>