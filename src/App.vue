<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
      <forloop/>
      <Luke/>
      <caleb/>
      <Ed/>
      <Jacob/>
      <Andrew/>
      <HelloWorld/>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import Andrew from './components/Andrew';
import Jacob from './components/Jacob';
import Ed from './components/Ed';
import caleb from './components/caleb';
import Luke from './components/Luke';
import forloop from './components/Concepts/ForLoop';

export default {
  name: 'App',

  components: {
    HelloWorld,
    Andrew,
    Jacob,
    Ed,
    caleb,
    Luke,
    forloop
  },


  data: () => ({
    //
  }),
};
</script>

<style>
  @import './css/vgrid.css';
</style>
