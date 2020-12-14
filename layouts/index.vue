<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      class="colored-bar"
      :mini-variant="miniVariant"
      :clipped="clipped"
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
      fixed
      app
    >
      <!-- <v-app-bar-nav-icon @click.stop="drawer = !drawer" /> -->
      <v-toolbar-title v-text="title" class='allura' />
      <v-spacer />
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <TheFooter/>
  </v-app>
</template>

<script>
import TheFooter from '~/components/UI/TheFooter.vue'

export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        // {
        //   icon: 'mdi-apps',
        //   title: 'Catalogo',
        //   to: '/'
        // },
        // {
        //   icon: 'mdi-chart-bubble',
        //   title: 'Lazos',
        //   to: '/lazos'
        // },
        // {
        //   icon: 'mdi-chart-bubble',
        //   title: 'Mochilas',
        //   to: '/mochilas'
        // },
        // {
        //   icon: 'mdi-chart-bubble',
        //   title: 'Peluches',
        //   to: '/peluches'
        // },
        // {
        //   icon: 'mdi-chart-bubble',
        //   title: 'Llaveros',
        //   to: '/llaveros'
        // },
        // {
        //   icon: 'mdi-chart-bubble',
        //   title: 'Monederos',
        //   to: '/monederos'
        // }
      ],
      miniVariant: false,
      right: false,
      rightDrawer: false,
      title: "Anayná: Girls' Accessories"
    }
  },
  components: {
    TheFooter
  }
}
</script>

<style>
.colored-bar{
  background-image:"~assets/images/bg.png"
}
.allura {
  font-family: Allura;
  font-size: 200%;
}
</style>
