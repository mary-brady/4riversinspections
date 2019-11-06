<template>
  <div class="contact">
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <p>this is a contact page!!!!</p>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "contact",
  components: {
    HelloWorld
  }
};
</script>
