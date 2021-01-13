<template>
  <v-container>
    <h2>Selectionner le format d'entée</h2>

    <v-card
      class="d-flex justify-space-around align-center"
      color="grey lighten-1"
      height="50vh"
    >
      <v-radio-group row>
        <v-card
          :key="type"
          v-for="type in types"
          width="50px"
          height="50px"
          color="grey lighten-6"
          ><v-radio></v-radio>
          <p>{{ type }}</p>
        </v-card>
        <!-- <v-card width="50px" height="50px" color="grey lighten-6"
          ><v-radio></v-radio
        ></v-card>
        <v-card width="50px" height="50px" color="grey lighten-6"
          ><v-radio></v-radio
        ></v-card> -->
      </v-radio-group>
    </v-card>
  </v-container>
</template>
<script>
export default {
  name: "StepOne",
  data: function () {
    return {
      types: ["files", "app", "api"],
    };
  },
};
</script>