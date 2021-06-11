<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      :clipped-left="clipped"
      color="indigo darken-4"
      fixed
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" color="white" />
      <v-toolbar-title v-text="title" />
      <v-spacer />
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    
    <Footer />
  </v-app>
</template>

<script>
import Footer from '~/layouts/footer.vue'

export default {
   components: {
    Footer
  },
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-ferry',
          title: 'じゅんちゃんとは？',
          to: '/'
        },
        {
          icon: 'mdi-book-open-page-variant',
          title: 'じゅんちゃんの活動',
          to: '/works'
        },
        {
          icon: 'mdi-youtube',
          title: 'youtube・twitter',
          to: '/youtube'
        },
        {
          icon: 'mdi-bee',
          title: '読書会',
          to: '/bookClub'
        },
        {
          icon: 'mdi-feather',
          title: 'お問い合わせ',
          to: '/contact'
        }
      ],
    }
  }
}
</script>
