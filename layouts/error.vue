<template>
  <div>
    <div class="py-12">
      <div class="text-center">
        <div v-if="error.statusCode === 404">
          <h1 class="error-title error--text">404</h1>
          <h3 class="text-uppercase error-subtitle" dark>PAGE NOT FOUND !</h3>
        </div>
        <div v-else>
          <h1 class="error-title error--text">404</h1>
          <h3 class="text-uppercase error-subtitle" dark>AN ERROR OCCURED!</h3>
        </div>

        <p class="text-muted mt-4 mb-4">
          YOU SEEM TO BE TRYING TO FIND HIS WAY HOME
        </p>
        <v-btn color="primary" to="/dashboard">Go to Dashboard</v-btn>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "EmptyLayout",
  layout: "blankLayout",
  props: {
    error: {
      type: Object,
      default: null,
    },
  },
  data() {
    return {
      pageNotFound: "404 Not Found",
      otherError: "An error occurred",
    };
  },
  head() {
    const title =
      this.error.statusCode === 404 ? this.pageNotFound : this.otherError;
    return {
      title,
    };
  },
};
</script>

<style lang="scss">
.error-title {
  font-size: 210px;
  font-weight: 900;
  text-shadow: 4px 4px 0 #fff, 6px 6px 0 #343a40;
  line-height: 210px;
}
</style>
