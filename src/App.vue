<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      flat
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

        <div class="text-h5 secondary--text">Aureus</div>
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

    <v-main>
      <Decision v-bind:title="titles"  :answers="answers"/>
    </v-main>
  </v-app>
</template>

<script>
import Decision from './components/Decision';

export default {
  name: 'App',

  components: {
    Decision
  },

  data: () => ({

    //question and answer data
    titles: ["Are you happy", "What are you"],
    answers: [["yes", "no"], ["male", "female"]]
  }),
};
</script>
