<template>

  <v-app>
    <div>
    <v-toolbar height="35px" dark>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Astroneer</v-toolbar-title>

      <v-spacer></v-spacer>

    </v-toolbar>

    <v-content>
      <HelloWorld/>
    </v-content>

    <v-content>
      <Article/>
    </v-content>

    <my-footer></my-footer>

    </div>
  </v-app>

</template>

<script>
import HelloWorld from './components/HelloWorld';
import Article from './components/Article';
import MyFooter from './components/MyFooter';

export default {
  components: {
    HelloWorld,
    Article,
    MyFooter,
  },
  data: () => ({

  }),
  created () {
    this.$vuetify.theme.dark = true
  },
}
</script>
