<template>
  <v-container>
    <v-row justify="center" align="center">
      <h2>じゅんちゃんの活動</h2>
      <v-timeline
        align-top
        :dense="$vuetify.breakpoint.smAndDown"
      >
        <v-timeline-item
          v-for="(item, i) in items"
          :key="i"
          :color="item.color"
          :icon="item.icon"
          fill-dot
        >
          <v-card
            :color="item.color"
            dark
          >
            <v-card-title class="text-h6">
              <h2 class="text-h4 white--text font-weight-light">
                Title 1
              </h2>
            </v-card-title>
            <v-card-text class="white text--primary">
              <p>Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.</p>
              <v-btn
                :color="item.color"
                class="mx-0"
                outlined
              >
                Button
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
        },
        {
          color: 'blue',
          icon: 'mdi-twitter',
        },
        {
          color: 'purple darken-1',
          icon: 'mdi-bee',
        },
        {
          color: 'green lighten-1',
          icon: 'mdi-book',
        },
      ],
    }),
  }
</script>