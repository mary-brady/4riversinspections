<template>
  <div id="app">
    <div id="nav">
      <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <a class="navbar-brand pr-3" href="/#/">
          <strong>4RiversInspections</strong>
        </a>
        <button
          class="navbar-toggler"
          type="button"
          data-toggle="collapse"
          data-target="#navbarColor01"
          aria-controls="navbarColor01"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarColor01">
          <ul class="navbar-nav mr-auto">
            <li class="nav-item">
              <router-link to="/">Home</router-link>
            </li>&nbsp; &nbsp;
            <li class="nav-item">
              <router-link to="/Pricing">Pricing</router-link>
            </li>&nbsp; &nbsp;
            <li class="nav-item">
              <router-link to="/About">About Us</router-link>
            </li>&nbsp; &nbsp;
            <li class="nav-item">
              <router-link to="/Contact">Contact</router-link>
            </li>
          </ul>
        </div>
      </nav>
      <router-view />
    </div>
  </div>
</template>

<script>
export default {
  name: "App"
};
</script>

<style>
.navbar,
a {
  font-weight: bold;
  color: #ffffff;
  font-family: "Roboto", sans-serif;
}
.navbar-brand {
  font-size: x-large;
}
</style>
