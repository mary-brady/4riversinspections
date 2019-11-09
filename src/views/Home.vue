<template>
  <v-container>
    <v-layout>
      <v-container fluid>
        <v-row justify="center">
          <v-col cols="12">
            <v-img :src="images.logo"></v-img>
          </v-col>
        </v-row>
        <v-row justify="center">
          <v-col cols="12">
            <p>Inspecting homes as if they were our own, with decades of construction experience and thousands of inspections completed!</p>
          </v-col>
        </v-row>
      </v-container>
    </v-layout>
  </v-container>
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
      }
    };
  }
};
</script>
<style>
a {
  color: black;
}
.cards {
  background-color: rgb(34, 116, 165);
  align-items: center;
  height: 30vw;
  justify-content: space-between;
}
</style>
