<template>
  <v-container fill-height>
    <v-row>
      <v-col cols="12">
        <h3 class="text-h3 text-center white--text">
          Robotek Engeener Examen
        </h3>
      </v-col>
      <v-col>
        <StepManager />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import StepManager from '@/components/StepManager'
export default {
  name: 'Game',
  components: { StepManager },
  data: () => ({
    step: 1
  })
}
</script>