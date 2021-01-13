<template>
  <v-stepper v-model="e1">
    <v-stepper-header>
      <v-stepper-step :complete="e1 > 1" step="1"> Etape 1 </v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step :complete="e1 > 2" step="2"> Etape 2 </v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step step="3"> Etape 3 </v-stepper-step>
    </v-stepper-header>

    <v-stepper-items>
      <v-stepper-content step="1">
        <step-one />
        <v-btn color="primary" @click="e1 = 2"> Continue </v-btn>

        <v-btn text> Cancel </v-btn>
      </v-stepper-content>

      <v-stepper-content step="2">
        <step-two />
        <v-btn color="primary" @click="e1 = 3"> Continue </v-btn>
        <v-btn text> Cancel </v-btn>
      </v-stepper-content>

      <v-stepper-content step="3">
        <step-three />
        <v-btn color="primary" @click="e1 = 1"> Continue </v-btn>
        <v-btn text> Cancel </v-btn>
      </v-stepper-content>
    </v-stepper-items>
  </v-stepper>
</template>

<script>
import StepOne from "../components/Step/StepOne.vue";
import StepThree from "../components/Step/StepThree.vue";
import StepTwo from "../components/Step/StepTwo.vue";

export default {
  name: "Stepper",
  components: {
    StepOne,
    StepTwo,
    StepThree,
    StepOne,
  },
  data() {
    return {
      e1: 1,
    };
  },
};
</script>

<style>
</style>