<template>
  <v-container fluid>
    <v-row>
      <v-col cols="12">
        <v-img :src="images.logo" contain height="300" width="300"></v-img>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <h1 class="display-1">About Us</h1>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <h3>Tyra Rickman</h3>
        <h5>Marketing &amp; Office Director</h5>
      </v-col>
    </v-row>
    <p>Tyra is from a small ranching community in Eastern Oregon where she learned the meaning of “hard work” at an early age. After high school she went to College of Idaho where she obtained her Bachelor's of Science and played Women’s Basketball all four years. She then went on to further develop her career in marketing and ecommerce for the next six years. Through her developed education &amp; experience Tyra has everything it takes to give you the best experience within our business. In her free time you can find Tyra at the local CrossFit gym, hiking, hunting, or participating in all things outdoors.</p>
  </v-container>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "about",
  components: {
    HelloWorld
  },
  data() {
    return {
      images: {
        logo: require("../assets/4RILogo2.jpg")
      }
    };
  }
};
</script>