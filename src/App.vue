<template>
  <v-app>
    <v-app-bar app color="orange" dark>
      <div class="d-flex align-center">
        <v-btn to="/" text block>
          <v-img
            alt="Platform Logo"
            src="@/assets/save-money.png"
            transition="scale-transition"
            width="50"
          />
          <h1 id="Crowd">Крауд</h1>
        </v-btn>
      </div>

      <v-spacer></v-spacer>

      <v-btn href target="_blank" text>
        <span class="mr-2">Проекты</span>
      </v-btn>

      <v-btn href target="_blank" text>
        <span class="mr-2">Как это работает</span>
      </v-btn>

      <v-btn href target="_blank" text>
        <span class="mr-2">Партнёры</span>
      </v-btn>

      <v-btn to="/users" text>
        <span class="mr-2">Участники</span>
      </v-btn>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Войти</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>
    <div id="nav">
      <!-- <router-link to="/">Home</router-link> -->
    </div>
    <router-view />
    <Footer />
  </v-app>
</template>

<script>
import Footer from "./components/Footer";

export default {
  name: "App",

  components: {
    Footer,
  },

  data: () => ({
    //
  }),
};
</script>

<style scoped>
#Crowd {
  padding-left: 1rem;
}
.theme--dark.v-btn--active:hover::before,
.theme--dark.v-btn--active::before {
  opacity: 0;
}
</style>
