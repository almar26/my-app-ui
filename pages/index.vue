<template>
  <div class="d-flex align-center justify-center" style="height: 70vh">
    <v-sheet width="400" class="mx-auto">
      <v-card class="elevation-12 mx-auto">
        <v-toolbar dark color="primary">
          <v-toolbar-title>Login form</v-toolbar-title>
        </v-toolbar>
        <v-card-text>
          <v-form
            ref="form"
            v-model="valid"
            @submit.prevent="submit()"
            lazy-validation
          >
            <v-text-field
              outlined
              v-model="email"
              label="Email"
              prepend-inner-icon="mdi-account"
            ></v-text-field>
            <v-text-field
              outlined
              v-model="password"
              label="Password"
              prepend-inner-icon="mdi-lock"
              type="password"
            >
            </v-text-field>
            <a href="#" class="text-body-2 font-weight-regular"
              >Forgot Password</a
            >
            <v-btn block class="mt-2" color="primary" to="/dashboard">Sign in</v-btn>
          </v-form>
        </v-card-text>
      </v-card>
    </v-sheet>
  </div>
</template>

<script>
export default {
  layout: "auth",
  name: "IndexPage",
  data() {
    return {
      valid: true,
      email: '',
      password: ''
    }
  }
};
</script>
