<template>
  <v-app style="background: white;">
    <v-navigation-drawer v-model="drawer" app>
      <v-list>
        <v-list-item v-for="item in items" :key="item.title" :to="{name:item.link}">
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app color="#51b6fd">
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="headline black--text text-uppercase">4RiversInspections</v-toolbar-title>
    </v-app-bar>

    <v-content>
      <router-view />
    </v-content>
    <v-footer color="#51b6fd" app>
      <span class="white--text">&copy; 4RiversTeamInspections 2019</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      drawer: false,
      items: [
        { title: "Home", icon: "mdi-home", link: "home" },
        { title: "Pricing", icon: "mdi-currency-usd", link: "pricing" },
        { title: "Contact", icon: "mdi-send", link: "Contact" },
        { title: "About Us", icon: "mdi-account-heart", link: "About" }
      ],
      images: {
        logo: require("./assets/4RILogo1.jpg")
      },
      mini: true
    };
  }
};
</script>