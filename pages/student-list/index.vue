<template>
  <v-container fluid>
    <v-row>
      <v-col>
        <h3>
          <v-icon left>mdi-format-list-bulleted-square</v-icon> List of Students
        </h3>
      </v-col>
      <v-col align="right">
        <v-tooltip bottom>
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              color="primary"
              right
              to="/machine/add"
              v-bind="attrs"
              v-on="on"
            >
              <v-icon>mdi-plus</v-icon>
              Add Student
            </v-btn>
          </template>
          <span align-center>Add Student</span>
        </v-tooltip>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-card elevation="0">
          <v-card-title>
            <v-spacer></v-spacer>
            <v-spacer></v-spacer>
            <v-spacer></v-spacer>
            <v-spacer></v-spacer>
            <v-text-field
              v-model="search"
              dense
              append-icon="mdi-magnify"
              label="Search"
              single-line
              hide-details
            ></v-text-field>
          </v-card-title>

          <v-data-table :headers="headers" :items="desserts" :search="search">
            <template slot="item.actions" slot-scope="{ item }">
              <v-btn
                color="primary"
                small
                depressed
                :to="`/student-list/${item.id}`"
              >
                <v-icon small left>mdi-open-in-new</v-icon>
                View
              </v-btn>
              <v-btn color="info" small depressed>
                <v-icon small left>mdi-pencil</v-icon>
                Edit
              </v-btn>
              <v-btn color="error" small depressed>
                <v-icon small left>mdi-delete</v-icon>
                Delete
              </v-btn>
            </template>
          </v-data-table>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
export default {
  data() {
    return {
      search: "",
      headers: [
        {
          text: "Dessert (100g serving)",
          align: "start",
          sortable: false,
          value: "name",
        },
        { text: "Calories", sortable: false, value: "calories" },
        { text: "Fat (g)", sortable: false, value: "fat" },
        { text: "Carbs (g)", sortable: false, value: "carbs" },
        { text: "Protein (g)", sortable: false, value: "protein" },
        { text: "Iron (%)", sortable: false, value: "iron" },
        { text: "", align: "end", sortable: false, value: "actions" },
      ],
      desserts: [
        {
          id: 1,
          name: "Frozen Yogurt",
          calories: 159,
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          iron: 1,
        },
        {
          id: 2,
          name: "Ice cream sandwich",
          calories: 237,
          fat: 9.0,
          carbs: 37,
          protein: 4.3,
          iron: 1,
        },
        {
          id: 3,
          name: "Eclair",
          calories: 262,
          fat: 16.0,
          carbs: 23,
          protein: 6.0,
          iron: 7,
        },
        {
          id: 4,
          name: "Cupcake",
          calories: 305,
          fat: 3.7,
          carbs: 67,
          protein: 4.3,
          iron: 8,
        },
        {
          id: 5,
          name: "Gingerbread",
          calories: 356,
          fat: 16.0,
          carbs: 49,
          protein: 3.9,
          iron: 16,
        },
        {
          id: 6,
          name: "Jelly bean",
          calories: 375,
          fat: 0.0,
          carbs: 94,
          protein: 0.0,
          iron: 0,
        },
        {
          id: 7,
          name: "Lollipop",
          calories: 392,
          fat: 0.2,
          carbs: 98,
          protein: 0,
          iron: 2,
        },
        {
          id: 8,
          name: "Honeycomb",
          calories: 408,
          fat: 3.2,
          carbs: 87,
          protein: 6.5,
          iron: 45,
        },
        {
          id: 9,
          name: "Donut",
          calories: 452,
          fat: 25.0,
          carbs: 51,
          protein: 4.9,
          iron: 22,
        },
        {
          id: 10,
          name: "KitKat",
          calories: 518,
          fat: 26.0,
          carbs: 65,
          protein: 7,
          iron: 6,
        },
      ],
    };
  },
};
</script>