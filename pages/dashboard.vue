<template>
  <v-container fluid>
    <v-row justify="center" align="center">
      <v-col cols="12" sm="3" md="3">
        <v-card elevation="0">
          <v-list-item>
            <v-list-item-content align="left">
              <v-list-item-subtitle class="subtitle mb-1">
                Active Student
              </v-list-item-subtitle>
              <div>
                <v-divider></v-divider>
                <v-list-item-subtitle class="display-1">
                  <div>32</div>
                </v-list-item-subtitle>
              </div>
            </v-list-item-content>
            <v-icon class="display-3" color="green"
              >mdi-account-badge-outline</v-icon
            >
          </v-list-item>
        </v-card>
      </v-col>
      <v-col cols="12" sm="3" md="3">
        <v-card elevation="0">
          <v-list-item>
            <v-list-item-content align="left">
              <v-list-item-subtitle class="subtitle mb-1">
                Innactive Student
              </v-list-item-subtitle>

              <div>
                <v-divider></v-divider>
                <v-list-item-subtitle class="display-1">
                  8
                </v-list-item-subtitle>
              </div>
            </v-list-item-content>
            <v-icon class="display-3" color="blue-grey"
              >mdi-account-cancel-outline</v-icon
            >
          </v-list-item>
        </v-card>
      </v-col>
      <v-col cols="12" sm="3" md="3">
        <v-card elevation="0">
          <v-list-item>
            <v-list-item-content align="left">
              <v-list-item-subtitle class="subtitle mb-1">
                Failed Student
              </v-list-item-subtitle>

              <div>
                <v-divider></v-divider>
                <v-list-item-subtitle class="display-1">
                  12
                </v-list-item-subtitle>
              </div>
            </v-list-item-content>
            <v-icon class="display-3" color="red"
              >mdi-account-remove-outline</v-icon
            >
          </v-list-item>
        </v-card>
      </v-col>
      <v-col cols="12" sm="3" md="3">
        <v-card elevation="0">
          <v-list-item>
            <v-list-item-content align="left">
              <v-list-item-subtitle class="subtitle mb-1">
                Dropped
              </v-list-item-subtitle>

              <div>
                <v-divider></v-divider>
                <v-list-item-subtitle class="display-1">
                  5
                </v-list-item-subtitle>
              </div>
            </v-list-item-content>
            <v-icon class="display-3" color="orange"
              >mdi-account-off-outline</v-icon
            >
          </v-list-item>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-card elevation="0">
          <v-card-title>
            Nutrition
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

          <v-data-table
            :headers="headers"
            :items="desserts"
            :search="search"
          ></v-data-table>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "DashboardPage",
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
        { text: "Calories", value: "calories" },
        { text: "Fat (g)", value: "fat" },
        { text: "Carbs (g)", value: "carbs" },
        { text: "Protein (g)", value: "protein" },
        { text: "Iron (%)", value: "iron" },
      ],
      desserts: [
        {
          name: "Frozen Yogurt",
          calories: 159,
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          iron: 1,
        },
        {
          name: "Ice cream sandwich",
          calories: 237,
          fat: 9.0,
          carbs: 37,
          protein: 4.3,
          iron: 1,
        },
        {
          name: "Eclair",
          calories: 262,
          fat: 16.0,
          carbs: 23,
          protein: 6.0,
          iron: 7,
        },
        {
          name: "Cupcake",
          calories: 305,
          fat: 3.7,
          carbs: 67,
          protein: 4.3,
          iron: 8,
        },
        {
          name: "Gingerbread",
          calories: 356,
          fat: 16.0,
          carbs: 49,
          protein: 3.9,
          iron: 16,
        },
        {
          name: "Jelly bean",
          calories: 375,
          fat: 0.0,
          carbs: 94,
          protein: 0.0,
          iron: 0,
        },
        {
          name: "Lollipop",
          calories: 392,
          fat: 0.2,
          carbs: 98,
          protein: 0,
          iron: 2,
        },
        {
          name: "Honeycomb",
          calories: 408,
          fat: 3.2,
          carbs: 87,
          protein: 6.5,
          iron: 45,
        },
        {
          name: "Donut",
          calories: 452,
          fat: 25.0,
          carbs: 51,
          protein: 4.9,
          iron: 22,
        },
        {
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
