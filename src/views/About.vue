<template>
  <v-container fluid>
    <v-row justify="center">
      <v-col cols="12" align="center">
        <v-img :src="images.logo" contain height="200" width="200"></v-img>
      </v-col>
    </v-row>
    <v-row justify="center">
      <v-col cols="12" align="center">
        <h1>About Us</h1>
      </v-col>
    </v-row>
    <v-row justify="center">
      <v-col cols="12" align="center">
        <h3>Tyra Rickman</h3>
        <h5>Marketing &amp; Office Director</h5>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" align="center">
        <v-img :src="images.tyra" contain height="300" width="400"></v-img>
      </v-col>
    </v-row>
    <v-row justify="center">
      <v-col :cols="[$vuetify.breakpoint.mdAndDown ? 12 : 6]" align="center">
        <p>Tyra is from a small ranching community in Eastern Oregon where she learned the meaning of “hard work” at an early age. After high school, she went to College of Idaho where she obtained her Bachelor's of Science and played women’s basketball all four years. She then went on to further develop her career in marketing and e-commerce for the next six years.</p>
        <p>Through her developed education &amp; experience, Tyra has everything it takes to give you the best experience within our business. In her free time, you can find Tyra at the local CrossFit gym, hiking, hunting, or participating in all things outdoors.</p>
      </v-col>
    </v-row>
    <v-row justify="center">
      <v-col cols="12" align="center">
        <h3>Sean Lowe</h3>
        <h5>Certified Inspector</h5>
      </v-col>
      <v-row>
        <v-col cols="12" align="center">
          <v-img :src="images.sean" contain height="300" width="400"></v-img>
        </v-col>
      </v-row>
    </v-row>
    <v-row justify="center">
      <v-col :cols="[$vuetify.breakpoint.mdAndDown ? 12 : 6]" align="center">
        <p>Sean grew up in Southern California where he went to high-school and community college. He is ASHI certified and has completed well over 1,500 inspections over the last 4 years in the Treasure Valley. He has been involved in many home remodeling experiences and has extensive knowledge of renovation and repairs. He has previous experience with commercial damage assessment and reporting as well.</p>
        <p>Sean loves this career because he gets to help his clients make an informed decision on a huge investment. When Sean isn't working you can find him at home with his lovely wife, newborn, two cats and dog. His other interests are hiking, camping, rafting and enjoying his saltwater reef fish tank.</p>
      </v-col>
    </v-row>
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
        logo: require("../assets/4RILogo2.jpg"),
        tyra: require("../assets/HeadShot.jpg"),
        sean: require("../assets/SeanHeadshot.jpg")
      }
    };
  }
};
</script>