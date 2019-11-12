<template>
  <v-layout>
    <v-container fluid>
      <v-row justify="center">
        <v-col cols="12" align="center">
          <v-img :src="images.logo" contain height="200" width="200"></v-img>
        </v-col>
      </v-row>
      <v-row justify="center">
        <v-col cols="12">
          <h1>About Us</h1>
        </v-col>
      </v-row>
      <v-row justify="center">
        <v-col cols="12" align="center">
          <h3>Tyra Rickman</h3>
          <h5>Marketing &amp; Office Director</h5>
        </v-col>
      </v-row>
      <p>Tyra is from a small ranching community in Eastern Oregon where she learned the meaning of “hard work” at an early age. After high school, she went to College of Idaho where she obtained her Bachelor's of Science and played women’s basketball all four years. She then went on to further develop her career in marketing and e-commerce for the next six years.</p>
      <p>Through her developed education &amp; experience, Tyra has everything it takes to give you the best experience within our business. In her free time, you can find Tyra at the local CrossFit gym, hiking, hunting, or participating in all things outdoors.</p>
    </v-container>
  </v-layout>
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