<template>
  <v-card>
    <v-card-title>Choose a form factor</v-card-title>
    <v-card-text>
      <v-row>
        <v-col cols="12" md="4" v-for="(type, index) in types" :key="'type' + index">
          <v-card 
            :color="selectedType === index ? 'primary' : 'white'" 
            @click="selectedType = index"
            :dark="selectedType === index"
          >
            <v-card-title>
              {{ type.name }}
            </v-card-title>
            <v-card-text>
              {{ type.description }}
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12">
          <v-select v-model="selectedMaterial" :items="materials" label="Material"></v-select>
        </v-col>
      </v-row>
    </v-card-text>
    <v-card-actions>
      <v-spacer></v-spacer>
      <v-btn color="primary" @click="$emit('next')" :disabled="!selectedType && !selectedMaterial">Continue</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  name: 'StepIntro',
  data: () => ({
    selectedType: null,
    types: [
      {name: 'Small', description: 'Good to build a fast robot', slots: 2, value: 30},
      {name: 'Medium', description: 'Good to build any robot type', slots: 3, value: 60},
      {name: 'Heavy', description: 'Good to build a resistant robot', slots: 4, value: 90}
    ],
    selectedMaterial: null,
    materials: [
      {text: 'Fer', value: 1.2},
      {text: 'Metal', value: 1},
      {text: 'Carbon', value: 0.8}
    ]
  })
}
</script>

<style>

</style>