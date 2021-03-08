<template>
  <v-app>
    <v-app-bar
      app
      color="success"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="9pay Logo"
          class="shrink mr-2"
          contain
          src="https://9mobile.com.ng/wp-content/uploads/2020/08/logo3.png"
          transition="scale-transition"
          width="40"
        />

        <v-span
          alt="9pay Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        >
        9pay
        </v-span>
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="/"
        target="_blank"
        text
      >
        <span class="mr-2">Login</span>
        <v-icon>mdi-lock-open</v-icon>
      </v-btn>
      <v-btn
        href="/"
        target="_blank"
        text
      >
        <span class="mr-2">Register</span>
        <v-icon>mdi-account-lock</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <HomePage/>
    </v-main>
  </v-app>
</template>

<script>
import HomePage from './components/HomePage';

export default {
  name: 'App',

  components: {
    HomePage,
  },

  data: () => ({
    //
  }),
};
</script>
