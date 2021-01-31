<template>
  <v-container>
    <v-row align="center" justify="center">
      <v-col cols="12">
        <v-hover v-slot="{ hover }" disabled>
          <v-card
            :elevation="hover ? 12 : 5"
            class="mx-auto"
            height="1500"
            max-width="800"
          >
            <v-card-text class="my-4 text-left title">
              Find:
              <vue-dropdown :config="config_dropdown"> </vue-dropdown>

              <br />
              My Jobs
              <v-row no-gutters align="center">
                <v-col cols="2" align="center">
                  <v-img
                    class="img-align"
                    lazy-src="@/assets/avatar1.png"
                    max-height="100"
                    max-width="100"
                    src="@/assets/avatar1.png"
                  ></v-img>
                </v-col>
                <v-col cols="2" align="center">
                  <v-img
                    class="img-align"
                    lazy-src="@/assets/avatar.png"
                    max-height="100"
                    max-width="100"
                    src="@/assets/avatar.png"
                  ></v-img>
                </v-col>
                <v-col cols="2" align="center">
                  <v-img
                    class="img-align"
                    lazy-src="@/assets/avatar2.png"
                    max-height="100"
                    max-width="100"
                    src="@/assets/avatar2.png"
                  ></v-img>
                </v-col>
                <v-col cols="2" align="center">
                  <v-img
                    class="img-align"
                    lazy-src="@/assets/avatar3.png"
                    max-height="100"
                    max-width="100"
                    src="@/assets/avatar3.png"
                  ></v-img>
                </v-col>
                <v-col cols="2" align="center">
                  <v-img
                    class="img-align"
                    lazy-src="@/assets/avatar4.png"
                    max-height="100"
                    max-width="100"
                    src="@/assets/avatar4.png"
                  ></v-img>
                </v-col>
                <v-col cols="2" align="center">
                  <v-img
                    class="img-align"
                    lazy-src="@/assets/avatar5.png"
                    max-height="100"
                    max-width="100"
                    src="@/assets/avatar5.png"
                  ></v-img>
                </v-col>
              </v-row>

              <br /><br />
              My Request
              <v-row no-gutters align="center">
                <v-col cols="2" align="center">
                  <v-img
                    class="img-align"
                    lazy-src="@/assets/avatar6.png"
                    max-height="100"
                    max-width="100"
                    src="@/assets/avatar6.png"
                  ></v-img>
                </v-col>
                <v-col cols="2" align="center">
                  <v-img
                    class="img-align"
                    lazy-src="@/assets/avatar7.png"
                    max-height="100"
                    max-width="100"
                    src="@/assets/avatar7.png"
                  ></v-img>
                </v-col>
                <v-col cols="2" align="center">
                  <v-img
                    class="img-align"
                    lazy-src="@/assets/avatar8.png"
                    max-height="100"
                    max-width="100"
                    src="@/assets/avatar8.png"
                  ></v-img>
                </v-col>
                <v-col cols="2" align="center">
                  <v-img
                    class="img-align"
                    lazy-src="@/assets/avatar9.png"
                    max-height="100"
                    max-width="100"
                    src="@/assets/avatar9.png"
                  ></v-img>
                </v-col>
                <v-col cols="2" align="center">
                  <v-img
                    class="img-align"
                    lazy-src="@/assets/avatar10.png"
                    max-height="100"
                    max-width="100"
                    src="@/assets/avatar10.png"
                  ></v-img>
                </v-col>
              </v-row>

              <br><br>
              Homework Tutoring
              <v-row no-gutters align="center">
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar11.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar11.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar12.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar12.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar13.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar13.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar14.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar14.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar1.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar1.png"
                    ></v-img>
                  </v-col>

                </v-row>

              <v-row no-gutters align="center">
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar2.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar2.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar3.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar3.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar4.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar4.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar5.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar5.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar6.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar6.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar7.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar7.png"
                    ></v-img>
                  </v-col>

                </v-row>


                <br><br>
              Interest Class
              <v-row no-gutters align="center">
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar11.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar11.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar12.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar12.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar13.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar13.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar14.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar14.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar1.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar1.png"
                    ></v-img>
                  </v-col>

                </v-row>

              <v-row no-gutters align="center">
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar2.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar2.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar3.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar3.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar4.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar4.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar5.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar5.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar7.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar7.png"
                    ></v-img>
                  </v-col>

                </v-row>

                <br><br>
              Paramedics
              <v-row no-gutters align="center">
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar11.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar11.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar12.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar12.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar13.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar13.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar14.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar14.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar1.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar1.png"
                    ></v-img>
                  </v-col>

                </v-row>

              <v-row no-gutters align="center">
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar2.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar2.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar6.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar6.png"
                    ></v-img>
                  </v-col>
                  <v-col cols="2" align="center">
                    <v-img
                      class="img-align"
                      lazy-src="@/assets/avatar7.png"
                      max-height="100"
                      max-width="100"
                      src="@/assets/avatar7.png"
                    ></v-img>
                  </v-col>

                </v-row>

            </v-card-text>
          </v-card>
        </v-hover>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import VueDropdown from "vue-dynamic-dropdown";

export default {
  name: "Dashboard",
  components: {
    VueDropdown,
  },
  data: function () {
    return {
      config_dropdown: {
        placeholder: "Please select a category",
        options: [
          {
            value: "Homework Tutoring",
          },
          {
            value: "Interest Class",
          },
          {
            value: "Paramedics",
          },
          {
            value: "Decoration",
          },
          {
            value: "Repair",
          },
          {
            value: "Cleaning",
          },
        ],
        prefix: "",
        backgroundColor: "",
      },
    };
  },
};
</script>
