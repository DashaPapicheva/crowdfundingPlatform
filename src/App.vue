<template>
  <v-app>
    <v-app-bar
      app
      color="orange"
      dark
    >

      <div class="d-flex align-center">
        <v-img
          alt="Platform Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href
        target="_blank"
        text
      >
        <span class="mr-2">Проекты</span>
      </v-btn>

      <v-btn
        href
        target="_blank"
        text
      >
        <span class="mr-2">Как это работает</span>
      </v-btn>

      <v-btn
        href
        target="_blank"
        text
      >
        <span class="mr-2">Партнёры</span>
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

    <!-- <v-content>
      <HelloWorld/>
    </v-content> -->
    <!-- <Footer/> -->
    <div id="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/users">Users</router-link>
    </div>
    <router-view/>
  </v-app>
</template>

<script>
// import HelloWorld from './components/HelloWorld';
// import Footer from './components/Footer';

export default {
  name: 'App',

  // components: {
  //   HelloWorld,
  //   Footer,
  // },

  data: () => ({
    //
  }),
};
</script>
