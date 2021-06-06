<template>
  <v-stepper
    v-model="step"
  >
    <v-stepper-step
      :complete="step > 1"
      step="1"
    >
      Introduction
      <small>Summarize if needed</small>
    </v-stepper-step>

    <v-stepper-content step="1">
      <StepIntro @next="step = 2"/>
    </v-stepper-content>

    <v-stepper-step
      :complete="step > 2"
      step="2"
    >
      Form Factor
    </v-stepper-step>

    <v-stepper-content step="2">
      <StepFormFactor @next="step = 3"/>
    </v-stepper-content>

    <v-stepper-step
      :complete="step > 3"
      step="3"
    >
      Armements
    </v-stepper-step>

    <v-stepper-content step="3">
      <StepFormFactor @next="step = 4"/>
    </v-stepper-content>

    <v-stepper-step step="4">
      Hardware
    </v-stepper-step>
    <v-stepper-content step="4">
      <StepFormFactor @next="step = 5"/>
    </v-stepper-content>
    <v-stepper-step step="4">
      Software
    </v-stepper-step>
    <v-stepper-content step="5">
      <StepFormFactor @next="step = 1"/>
    </v-stepper-content>
  </v-stepper>
</template>

<script>
import StepIntro from '@/components/Steps/StepIntro'
import StepFormFactor from '@/components/Steps/StepFormFactor'

export default {
  name: 'StepManager',
  components: { StepIntro, StepFormFactor },
  data: () => ({
    step: 1
  })
}
</script>

<style>

</style>