<template>
  <v-app style="background-color: #4c6ef5;">
    <v-app-bar
      app
      color="transparent"
      dark
      flat
    >
      <v-toolbar-title>
        Robotek Inc.
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text to="/about">wtf?</v-btn>
    </v-app-bar>

    <v-main>
      <v-fade-transition mode="out-in">
        <router-view/>
      </v-fade-transition>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
