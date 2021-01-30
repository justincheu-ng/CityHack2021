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
              <div><h2>Matching Result</h2></div>

              <br />

              <div>
                <v-row no-gutters align="center">
                  <v-col cols="4" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar.png"
                      max-height="120"
                      max-width="120"
                      src="@/assets/avatar.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="8" align="left">
                    Chan Siu Han, Carmen

                    <br /><br />
                    <div align="left">
                      <ul>
                        <li>Responsible</li>
                        <li>Patient</li>
                        <li>5 years of experience in Web Development</li>
                      </ul>
                    </div>
                  </v-col>
                </v-row>
              </div>

              <br /><br />
              <div class="text-center">
                <!--v-btn v-on:click="nextQuestion" rounded color="primary" dark> Next </v-btn-->
                <v-btn
                  v-on:click="confirmYes"
                  class="mx-2"
                  fab
                  dark
                  large
                  color="green"
                >
                  <v-icon dark> mdi-check-bold </v-icon>
                </v-btn>
                &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

                <v-btn
                  v-on:click="confirmNo"
                  class="mx-2"
                  fab
                  dark
                  large
                  color="red"
                >
                  <v-icon medium>X</v-icon>
                </v-btn>
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
  name: "Confirm",
  methods: {
    confirmYes: function () {
      console.log("clicked Yes");
    },
    confirmNo: function () {
      console.log("clicked No");
    },
  },
};
</script>
