<template>
  <v-card>
    <v-card-title>The Exam</v-card-title>
    <v-card-text>
      Welcome to the Robotek engineering exam. Passing this exam is mandatory in order to obtain the license allowing you to join the Robotek league.
    </v-card-text>
    <v-card-title>The Robotek League</v-card-title>
    <v-card-text>
      The Robotek League is where thousands of robotics engineers compete against each other with the robots they build.
    </v-card-text>
    <v-card-title>The Rules</v-card-title>
    <v-card-text>
      Robots are built, configured and programmed using the Robotek framework. For this exam, you will have to design your own robot and have it fight in the arena.
You get your license if your robot wins.
    </v-card-text>
    <v-card-actions>
      <v-spacer></v-spacer>
      <v-btn color="primary" @click="$emit('next')">Continue</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  name: 'StepIntro'
}
</script>

<style>

</style>