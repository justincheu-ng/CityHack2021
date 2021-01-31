
//Login.vue

<template>
  <section class="section-container">
    <v-row class="signin">
      <v-col cols="4" class="left">
        <h2>LOGIN</h2>
        <validation-observer ref="observer">
           <v-form  @submit="sub">
            <validation-provider v-slot="{ errors }" v-model="email" >
              <v-text-field
                :error-messages="errors"
                label="Email"
                v-model="email"
              ></v-text-field>
            </validation-provider>
            <validation-provider v-slot="{ errors }" v-model="password">
              <v-text-field
                :error-messages="errors"
                label="Password"
                :type="showPass ? 'text' : 'password'"
                v-model="password"
              ></v-text-field>
            </validation-provider>
            <div class="text-center">
              <v-btn class="signin-btn" type="submit" rounded color="blue" dark>
                Sign In
              </v-btn>
            </div>
          </v-form>
        </validation-observer>
      </v-col>
    </v-row>
  </section>
</template>



<script>
import { ValidationProvider, setInteractionMode, ValidationObserver } from 'vee-validate'

setInteractionMode('eager')

export default {
  components: {
    ValidationProvider,
    ValidationObserver
  },
   data() {
    return {
    email: "",
    password: "",
    showPass: false
   };
  },
  methods:{
  sub() {
      var json = require('../../data.json');
      console.log(this.email);
                if(this.email != "" && this.password != "") {
                    if(this.email == json.email && this.password == json.password) {
                        console.log("The email and password is authenticated");
                        this.$emit("authenticated", true);
                        this.$router.replace({ name: "secure" });
                    } else {
                        console.log("The email or password is incorrect");
                    }
                } else {
                    console.log("An email and password must be present");
                }
            }
          }
    }
</script>

<style>
/* ./assets/styles.scss */

.section-container {
  padding: 125px;
  margin: 125px;
  background: #fff;
  width: 200%;
  box-shadow: 0 0 1px 1px rgba($color: #000000, $alpha: 0.1);
  box-sizing: border-box;
  .signin {
    padding: 0px;
    max-width: 800px;
    margin: 0 auto;
    min-height: 130px;
    box-shadow: 0 0 1px 1px rgba($color: #000000, $alpha: 0.1);
    .left {
      padding: 0px;
      justify-content: center;
      align-items: center;
      box-sizing: border-box;
      display: flex;
      color: #30ac7c;
      background-color: #f9f9f9;
    }
    .right {
      padding: 30px;
      box-sizing: border-box;
      background: #30ac7c;
      color: #fff;
      h2 {
        text-align: center;
        margin: 30px 0;
      }
      .signin-btn {
        width: 100%;
        color: #30ac7c;
      }
    }
  }
}


</style>