<template>
  <v-container fluid>
    <h1>DIT 3A Prelim Exam</h1>
    <v-row class="mt-3" >
      <v-col cols="12" md="4">
        <v-card elevation="0">
          <v-card-title> Forms </v-card-title>
          <v-card-text>
            <v-form>
              <v-text-field label="Lastname" outlined ></v-text-field>
              <v-text-field label="Firstname" outlined ></v-text-field>
              <v-text-field label="Email Address" outlined ></v-text-field>
              <v-text-field label="Gender" outlined ></v-text-field>
            </v-form>
          </v-card-text>
          <v-card-actions>
            <v-btn color="success">Submit</v-btn>
            <v-spacer></v-spacer>
            <v-btn color="error">Cancel</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="12" md="8">
        <v-card elevation="0">
          <v-card-title>Tables</v-card-title>
          <v-data-table
            :headers="headers"
            :items="student_data"
            item-key="name"
            class="elevation-0"
          ></v-data-table>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
export default {
  data() {
    return {
      headers: [
        {
          text: "ID",
          align: "start",
          sortable: false,
          value: "id",
        },
        { text: "Lastname", value: "last_name" },
        { text: "Firstname", value: "first_name" },
        { text: "Email Address", value: "email" },
        { text: "Gender", value: "gender" },
      ],
      student_data: [
        {
          id: 1,
          first_name: "Abbie",
          last_name: "Murch",
          email: "amurch0@elegantthemes.com",
          gender: "Female",
        },
        {
          id: 2,
          first_name: "Dael",
          last_name: "Wearn",
          email: "dwearn1@elpais.com",
          gender: "Female",
        },
        {
          id: 3,
          first_name: "Harlin",
          last_name: "Wastall",
          email: "hwastall2@spiegel.de",
          gender: "Male",
        },
        {
          id: 4,
          first_name: "Jeannie",
          last_name: "Van der Veldt",
          email: "jvanderveldt3@gnu.org",
          gender: "Female",
        },
        {
          id: 5,
          first_name: "Teodoro",
          last_name: "Marston",
          email: "tmarston4@gov.uk",
          gender: "Male",
        },
        {
          id: 6,
          first_name: "Claybourne",
          last_name: "Leitch",
          email: "cleitch5@mashable.com",
          gender: "Male",
        },
        {
          id: 7,
          first_name: "Nehemiah",
          last_name: "Gregr",
          email: "ngregr6@com.com",
          gender: "Male",
        },
        {
          id: 8,
          first_name: "Odelle",
          last_name: "Greenset",
          email: "ogreenset7@newyorker.com",
          gender: "Female",
        },
        {
          id: 9,
          first_name: "Ardella",
          last_name: "Fullicks",
          email: "afullicks8@hugedomains.com",
          gender: "Female",
        },
        {
          id: 10,
          first_name: "Walsh",
          last_name: "Raulston",
          email: "wraulston9@hugedomains.com",
          gender: "Male",
        },
      ],
    };
  },
};
</script>