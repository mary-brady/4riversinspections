<template>
  <div class="container-fluid">
    <div class="row row justify-content-center">
      <div class="hero-image col-12">
        <img src="../assets/Home1.jpeg" alt="home" />
      </div>
    </div>
    <div class="row justify-content-center">
      <div class="col-lg-12">
        <p>Dedicated to serving Idaho home buyers and real estate agents. Our goal is to make the process of home inspection as convenient, thorough, and affordable as possible</p>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  components: {
    HelloWorld
  }
};
</script>
<style scoped>
.hero-image {
  align-content: center;
}
</style>
