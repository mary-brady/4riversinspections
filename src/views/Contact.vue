<template>
  <v-container>
    <v-layout>
      <v-container fluid>
        <v-row>
          <v-col cols="12">
            <h1 class="display-1">Contact Us!</h1>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="12">
            <p>We completely understand the magnitude of a home purchase and all of the questions that come with it. Please give us a call or send us an email. You’re family now, so feel free to contact us at any hour of the day or night. We will always be here for you!</p>
          </v-col>
        </v-row>
        <v-row align="center" no-gutters>
          <v-col cols="6">
            <h2>
              <u>CALL US</u>
            </h2>
          </v-col>
          <!-- <v-col cols="2">
            <i class="fas fa-phone-alt" style="font-size: x-large;"></i>
          </v-col>-->
        </v-row>
        <v-row>
          <v-col cols="12">
            <h4>
              <a href="tel:208-918-0805">(208) 918-0805</a>
            </h4>
          </v-col>
        </v-row>
        <v-row align="center" no-gutters>
          <v-col cols="8">
            <h2>
              <u>EMAIL US</u>
            </h2>
            <p>You can email us directly:</p>
          </v-col>
          <!-- <v-col cols="2">
            <i class="far fa-paper-plane" style="font-size: x-large;"></i>
          </v-col>-->
          <v-row align="center" justify="center" no-gutters>
            <v-col cols="12" justify="center">
              <h5>
                <a href="mailto:tyra@4riversinspections.com">tyra@4riversinspection.com</a>
              </h5>
            </v-col>
          </v-row>
          <v-row align="center" justify="center" no-gutters>
            <v-col cols="12" justify="center">
              <h5>
                <a href="mailto:sean@4riversinspections.com">sean@4riversinspection.com</a>
              </h5>
            </v-col>
          </v-row>
        </v-row>
        <!-- <v-row>
          <v-col cols="12">
            <form action>
              <v-text-field
                v-model="name"
                :error-messages="nameErrors"
                label="Name"
                required
                @input="$v.name.$touch()"
                @blue="$v.name.$touch()"
              ></v-text-field>
              <v-text-field
                v-model="email"
                :error-messages="emailErrors"
                label="Email"
                required
                @input="$v.email.$touch()"
                @blue="$v.email.$touch()"
              ></v-text-field>
              <v-text-field
                v-model="phone"
                :error-messages="phoneErrors"
                label="Phone Number"
                required
                @input="$v.phone.$touch()"
                @blue="$v.phone.$touch()"
              ></v-text-field>
              <v-btn class="mr-4" @click="submit">submit</v-btn>
              <v-btn class="mr-4" @click="clear">Clear Form</v-btn>
            </form>
          </v-col>
        </v-row>-->
      </v-container>
    </v-layout>
  </v-container>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
// import Vuelidate from "vuelidate";
// import { validationMixin } from "vuelidate";
const { validationMixin, default: Vuelidate } = require("vuelidate");
const { required, email, numeric } = require("vuelidate/lib/validators");

export default {
  name: "Contact",
  components: {
    HelloWorld
  },
  mixins: [validationMixin],
  validations: {
    name: { required },
    email: { required, email },
    phone: { required, numeric }
  },
  data: () => ({
    name: "",
    email: "",
    phone: ""
  }),
  computed: {
    nameErrors() {
      const errors = [];
      if (!this.$v.name.$dirty) return errors;
      !this.$v.name.required && errors.push("Name is required.");
      return errors;
    },
    emailErrors() {
      const errors = [];
      if (!this.$v.email.$dirty) return errors;
      !this.$v.email.email && errors.push("Must be a valid Email");
      !this.$v.email.required && errors.push("Email is required");
      return errors;
    },
    phoneErrors() {
      const errors = [];
      if (!this.$v.phone.$dirty) return errors;
      !this.$v.phone.required && errors.push("Phone is required");
      return errors;
    }
  },
  methods: {
    clear() {
      this.$v.reset();
      this.name = "";
      this.email = "";
      this.phone = "";
    },
    submit() {
      this.$store.dispatch("sendEmail", {
        name: this.name,
        phone: this.phone,
        email: this.email
      });
      clear();
    }
  }
};
</script>
