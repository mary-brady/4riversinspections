<template>
  <v-container fluid>
    <v-row justify="center">
      <v-col cols="12">
        <v-card>
          <v-card-title>
            <h4>Home Inspection Pricing</h4>
          </v-card-title>
          <v-divider></v-divider>
          <v-row>
            <v-col cols="6">
              <v-card-subtitle>Square Feet</v-card-subtitle>
            </v-col>
            <v-col cols="6">
              <v-card-subtitle>Price</v-card-subtitle>
            </v-col>
          </v-row>
          <v-divider></v-divider>
          <v-data-iterator :items="pricing" hide-default-footer>
            <v-list v-for="price in pricing" :key="price.ft" cols="12">
              <v-row justify="center">
                <v-col cols="6">
                  <v-list-item-content>{{price.ft}}</v-list-item-content>
                </v-col>
                <v-col cols="6">
                  <v-list-item-content class="align-end">{{price.price}}</v-list-item-content>
                </v-col>
              </v-row>
              <v-divider></v-divider>
            </v-list>
          </v-data-iterator>
        </v-card>
      </v-col>
    </v-row>
    <v-row justify="center">
      <v-col cols="12">
        <v-card>
          <v-card-title>
            <h4>Additional Services</h4>
          </v-card-title>
          <v-divider></v-divider>
          <v-row>
            <v-col cols="6">
              <v-card-subtitle>Service</v-card-subtitle>
            </v-col>
            <v-col cols="6">
              <v-card-subtitle>Price</v-card-subtitle>
            </v-col>
          </v-row>
          <v-divider></v-divider>
          <v-data-iterator :items="addService" hide-default-footer>
            <v-list v-for="service in addService" :key="service.service" cols="12">
              <v-row>
                <v-col cols="6">
                  <v-list-item-content>{{service.service}}</v-list-item-content>
                </v-col>
                <v-col cols="6">
                  <v-list-item-content class="align-end">{{service.price}}</v-list-item-content>
                </v-col>
              </v-row>
              <v-divider></v-divider>
            </v-list>
          </v-data-iterator>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
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
