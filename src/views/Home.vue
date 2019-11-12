<template>
  <v-layout>
    <v-container fluid>
      <v-row justify="center">
        <v-col cols="12" align="center">
          <v-img :src="images.logo" height="500" width="600"></v-img>
        </v-col>
      </v-row>
      <v-row justify="center">
        <v-col cols="12">
          <p>Inspecting homes as if they were our own, with decades of construction experience and thousands of inspections completed!</p>
        </v-col>
      </v-row>
      <v-list v-for="cont in content" :key="cont.title">
        <v-row justify="center">
          <v-col cols="12">
            <v-card shaped :elevation="3">
              <v-card-title>{{cont.title}}</v-card-title>
              <v-card-text>{{cont.text}}</v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-list>
    </v-container>
  </v-layout>
</template>

<script>
import HelloWorld from "../components/HelloWorld";

export default {
  name: "Home",

  components: {
    HelloWorld
  }
};
</script>
ate>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  components: {
    HelloWorld
  },
  data() {
    return {
      images: {
        logo: require("../assets/4RILogo1.jpg")
      },
      content: [
        {
          title: "Why Choose Us?",
          text:
            "When you choose us, you are family. As family, we keep the best interest of your investment at the forefront throughout our entire process. We love what we do and truly care about our customers. The impact of a home purchase is huge and we strive to NEVER treat you like another number on the books."
        },
        {
          title: "Inspections - Guaranteed!",
          text:
            "All of our inspections are guaranteed. If you are not 100% satisfied with your home inspection we will give you your money back."
        },
        {
          title: "Experience!",
          text:
            "Extensive background in the building industry, paired with over 2,000 inspections in Oregon & Idaho gives us an edge most don’t have."
        },
        {
          title: "Community",
          text:
            "We love when buyers join us on inspections and in most cases prefer it! As a home buyer we understand you will have questions, and find the best way to answer is in-person as they arise."
        }
      ]
    };
  }
};
</script>
<style scoped>
</style>
