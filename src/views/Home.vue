<template>
  <HelloWorld />
</template>

<script>
import HelloWorld from '../components/HelloWorld';

export default {
  name: 'Home',

  components: {
    HelloWorld,
  },
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
