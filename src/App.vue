<template>
  <v-app>
    <v-app-bar app color="dark" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn130.picsart.com/300572844038211.png?type=webp&to=min&r=240"
          transition="scale-transition"
          width="95"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src=""
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn to="/"  text>
        <span class="mr-2">Home</span>
      </v-btn>
       <v-btn to="/about"  text>
        <span class="mr-2">about</span>
      </v-btn>
       <v-btn to="/Todo"  text>
        <span class="mr-2">Todo</span>
      </v-btn>
    </v-app-bar>
    

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  }),
};
</script>
