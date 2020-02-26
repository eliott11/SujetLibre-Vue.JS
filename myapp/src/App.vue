<template>

  <div>

    <v-toolbar
            dark
            src=""
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Astroneer</v-toolbar-title>

      <v-spacer></v-spacer>

    
    </v-toolbar>

  <v-app>
    <v-content>
      <HelloWorld/>
    </v-content>
  </v-app>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld';

  export default {
    components: {
      HelloWorld
    },
    data: () => ({

    }),
    created () {
      this.$vuetify.theme.dark = true
    },
  }
</script>
