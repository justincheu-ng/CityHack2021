<template>
  <v-container>
    <v-row align="center" justify="center">
      <v-col cols="12">
        <v-hover v-slot="{ hover }" disabled>
          <v-card
            :elevation="hover ? 12 : 5"
            class="mx-auto"
            height="450"
            max-width="600"
          >
            <v-card-text class="my-4 text-center title">
              <div>
                {{ title[currentQuestion] }}
              </div>

              <div v-for="ans in answers[currentQuestion]" v-bind:key="ans">
                <br /><br />
                <v-btn elevation="2" outlined> {{ ans }} </v-btn>
              </div>
              <br /><br />
              <div v-if="(title.length - 1) != currentQuestion" class="text-right">
                <v-btn v-on:click="nextQuestion" rounded color="primary" dark> Next </v-btn>
              </div>
            </v-card-text>
          </v-card>
        </v-hover>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Decision",
  props: {"title": {}, 
  "answers": {
    type: Array
  }},
  data: () => ({
    currentQuestion: 0, 
  }),
  methods: {
    nextQuestion: function() {
      this.currentQuestion += 1
      //console.log("clicked" + this.currentQuestion)
    }
  }
};
</script>