<template>
  <v-container fill-height align-content-start>
    <v-row>
      <v-toolbar color="transparent" flat>
      <v-btn text dark @click="$router.back()">
        <v-icon left>mdi-keyboard-backspace</v-icon>
        Go back
      </v-btn>
    </v-toolbar>
    </v-row>
    <v-row>
      <v-col>
        <h2 class="text-h2 white--text text-center mt-10">This is a web game.</h2>
      </v-col>
    </v-row>
  </v-container>
</template>
