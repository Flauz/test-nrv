<template>
  <v-container
    ><h2>Selectionner le déclencheur</h2>
    <v-card class="mb-12" color="grey lighten-1" height="60vh">
      <h4>Choisissez le type de déclencheur pour mettre à jour les données</h4>
      <div>
        <v-select :items="items" filled label="Filled style"></v-select>
      </div>
      <div class="d-flex flex-column">
        <h4 class="justify-center">
          Choisissez la date de mise à jour attendue
        </h4>
        <div class="justify-center">
          <v-date-picker v-model="picker"></v-date-picker>
        </div>
      </div> </v-card
  ></v-container>
</template>
<script>
export default {
  name: "StepThree",

  data() {
    return {
      items: ["foo", "bar", "fizz", "buzz"],
      picker: new Date().toISOString().substr(0, 10),
    };
  },
  methods: {
    allowedDates: (val) => parseInt(val.split("-")[2], 10) % 2 === 0,
  },
};
</script>