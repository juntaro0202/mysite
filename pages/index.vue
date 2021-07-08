<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <div class="text-center">
        <main-logo />
        <h2>じゅんちゃんとは？</h2>
        <p>哲学書や教養書、古典を読み漁り、</p>
        <p>より良い社会とは何か、より良い生き方とは何かを考えています。</p>
        <p>youtubeで時事ネタを語ったり、読書会をしたり色々やってます。</p>
      </div>
    </v-col>
  </v-row>
</template>

<script>
import MainLogo from '~/components/MainLogo.vue'

export default {
  components: {
    MainLogo
  }
}
</script>
