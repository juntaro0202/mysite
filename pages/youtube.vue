<template>
  <v-container>
      <h2>youtubeとかチュイッターとか</h2>
      <p>
        <ul>哲学入門チャンネル</ul>
        <ul>時事ネタとか喋ってます。たまにライブしたり、会員さん限定の読書会もしてます。</ul>
      </p>
    <v-row>
      <iframe width="424" height="238"
        src="https://www.youtube.com/embed/cOPSH5VTFlw"
        title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
        clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen />

      <v-card class="mx-auto">
      <v-card-title>
        <v-icon large left color="#26c6da">mdi-twitter</v-icon>
      </v-card-title>
        <v-card-text class="text font-weight-bold">
        <Timeline :id="user_id" sourceType="profile" :options="{ tweetLimit: '3' }"/>
        </v-card-text>
      </v-card>
    </v-row>
  </v-container>
</template>

<script>
import { Timeline } from "vue-tweet-embed";
export default {
  components: {
    Timeline
  },
  data: function() {
    return {
      user_id: "junchann0202"
    };
  }
};
</script>