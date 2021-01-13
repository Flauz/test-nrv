<template>
  <v-container>
    <h2>Renseignez la carte</h2>
    <v-card class="align-center" color="grey lighten-1" height="60vh">
      <div>
        <dropzone />
        <div>
          <h3>Donner un nom à votre carte</h3>
          <v-text-field label="Solo" solo></v-text-field>
        </div>
        <div>
          <h3>Ajouter des étiquettes d'équipe</h3>
          <v-autocomplete
            v-model="values"
            :items="items"
            outlined
            dense
            chips
            small-chips
            label="Outlined"
            multiple
          ></v-autocomplete>
        </div>
      </div>
    </v-card>
  </v-container>
</template>
<script>
import Dropzone from "../Dropzone.vue";
export default {
  name: "StepTwo",
  components: {
    Dropzone,
  },
  data() {
    return {
      items: ["foo", "bar", "fizz", "buzz"],
      value: null,
    };
  },
};
</script>