<template>
  <v-container>
    <h1>Prelim Page</h1>
    <v-row class="mt-3">
      <v-col cols="12" md="4">
        <v-card elevation="12">
          <v-list-item>
            <v-list-item-content align="left">
              <v-list-item-subtitle class="display-1">
                DIT 3A
              </v-list-item-subtitle>
            </v-list-item-content>
            <v-icon class="display-3" color="green"
              >mdi-note-text</v-icon
            >
          </v-list-item>
          <v-card-actions class="mt-2"><v-btn elevation="0" block color="success" to="/exams/prelim/dit-3a">View Exams</v-btn></v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="12" md="4">
        <v-card elevation="12">
          <v-list-item>
            <v-list-item-content align="left">
              <v-list-item-subtitle class="display-1">
                DIT 3B
              </v-list-item-subtitle>
            </v-list-item-content>
            <v-icon class="display-3" color="blue"
              >mdi-note-text</v-icon
            >
          </v-list-item>
          <v-card-actions class="mt-2"><v-btn elevation="0" block color="blue" dark>View Exams</v-btn></v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="12" md="4">
        <v-card elevation="12">
          <v-list-item>
            <v-list-item-content align="left">
              <v-list-item-subtitle class="display-1">
                BSIT 4A
              </v-list-item-subtitle>
            </v-list-item-content>
            <v-icon class="display-3" color="orange"
              >mdi-note-text</v-icon
            >
          </v-list-item>
          <v-card-actions class="mt-2"><v-btn elevation="0" block color="orange" dark to="/exams/prelim/bsit-4a">View Exams</v-btn></v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>