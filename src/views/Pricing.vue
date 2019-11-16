<template>
  <v-layout>
    <v-container fluid>
      <v-row justify="center">
        <v-col :cols="[$vuetify.breakpoint.mdAndDown ? 12 : 6]">
          <v-card>
            <v-card-title>
              <h3>Home Inspection Pricing</h3>
            </v-card-title>
            <v-divider></v-divider>
            <v-row>
              <v-col :cols="[$vuetify.breakpoint.mdAndDown ? 8 : 8]">
                <v-card-subtitle class="font-weight-black">Square Feet</v-card-subtitle>
              </v-col>
              <v-col :cols="[$vuetify.breakpoint.mdAndDown ? 4 : 4]">
                <v-card-subtitle class="font-weight-black">Price</v-card-subtitle>
              </v-col>
            </v-row>
            <v-divider></v-divider>
            <v-list v-for="price in pricing" :key="price.ft">
              <v-row>
                <v-col :cols="[$vuetify.breakpoint.mdAndDown ? 8 : 8]">
                  <v-list-item>{{price.ft}}</v-list-item>
                </v-col>
                <v-col :cols="[$vuetify.breakpoint.mdAndDown ? 4 : 4]">
                  <v-list-item>{{price.price}}</v-list-item>
                </v-col>
              </v-row>
              <v-divider></v-divider>
            </v-list>
          </v-card>
        </v-col>
      </v-row>
      <v-row justify="center">
        <v-col :cols="[$vuetify.breakpoint.mdAndDown ? 12 : 6]">
          <v-card>
            <v-card-title>
              <h3>Addt. Services</h3>
            </v-card-title>
            <v-divider></v-divider>
            <v-row justify="center">
              <v-col :cols="[$vuetify.breakpoint.mdAndDown ? 6 : 6]" align="center">
                <v-card-subtitle>Service</v-card-subtitle>
              </v-col>
              <v-col :cols="[$vuetify.breakpoint.mdAndDown ? 6 : 6]" align="center">
                <v-card-subtitle>Price</v-card-subtitle>
              </v-col>
            </v-row>
            <v-divider></v-divider>
            <v-list v-for="service in addService" :key="service.service">
              <v-row justify="center">
                <v-col :cols="[$vuetify.breakpoint.mdAndDown ? 8 : 8]">
                  <v-list-item>{{service.service}}</v-list-item>
                </v-col>
                <v-col :cols="[$vuetify.breakpoint.mdAndDown ? 4 : 4]">
                  <v-list-item>{{service.price}}</v-list-item>
                </v-col>
              </v-row>
              <v-divider></v-divider>
            </v-list>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-layout>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "pricing",
  components: {
    HelloWorld
  },
  data() {
    return {
      pricing: [
        { ft: "1000 - 1500", price: "$350" },
        { ft: "1501 - 2000", price: "$375" },
        { ft: "2001 - 2500", price: "$350" },
        { ft: "2501 - 3000", price: "$350" },
        { ft: "3001 - 3500", price: "$350" },
        { ft: "3501 - 4000", price: "$350" },
        { ft: "4001 - 4500", price: "$350" }
      ],
      addService: [
        { service: "Infrared", price: "Add $50" },
        { service: "Radon Testing", price: "$125" },
        {
          service: "Well Water Quality & Flow Rate Testing",
          price: "$125 (Water Only)"
        },
        { service: "Asbestos & Lead Sampling", price: "Call for Quote!" },
        { service: "Mold Testing", price: "$295" },
        { service: "Healthy Home Check-ups", price: "Call for Quote!" },
        {
          service: "1-Year Builders Warranty Inspection",
          price: "$50 OFF Normal Home Pricing!"
        },
        { service: "Methamphetamine Testing", price: "$125" },
        { service: "Reinspection Post-Repairs", price: "FREE! (in most cases)" }
      ]
    };
  }
};
</script>

<style scoped>
@media only screen and (min-width: 300px) {
  .container {
    max-width: 280px;
  }
}
@media only screen and (min-width: 600px) {
  .container {
    max-width: 560px;
  }
}
@media only screen and (min-width: 960px) {
  .container {
    max-width: 900px;
  }
}
@media only screen and (min-width: 1264px) {
  .container {
    max-width: 1185px;
  }
}
@media only screen and (min-width: 1904px) {
  .container {
    max-width: 1785px;
  }
}
</style>
