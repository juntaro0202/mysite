<template>
  <v-container>
      <h2>youtubeとかチュイッターとか</h2>
      <ul>
        <li>哲学入門チャンネル</li>
        <li>時事ネタとか喋ってます。たまにライブしたり、会員さん限定の読書会もしてます。</li>
      </ul>
   
    <v-row>
      <v-col cols="9">
      <iframe width="424" height="238"
        src="https://www.youtube.com/embed/cOPSH5VTFlw"
        title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
        clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen />
      </v-col>

      <v-col cols="3">
        <v-card>
          <v-toolbar
            color="blue"
            dark
          >
          <v-toolbar-title>最新のチュイッター</v-toolbar-title>

            <v-spacer></v-spacer>
          <v-btn icon>
            <v-icon>mdi-twitter</v-icon>
          </v-btn>
          </v-toolbar>

          <v-card-text class="text font-weight-bold">
          <Timeline :id="user_id" sourceType="profile" :options="{ tweetLimit: '3' }"/>
          </v-card-text>
        </v-card>
      </v-col>
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

<style scoped>
ul {
  list-style: none;
}
</style>