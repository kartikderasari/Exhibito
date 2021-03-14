<template>
  <v-bottom-navigation
    v-model="value"
    app
    v-if="this.$vuetify.breakpoint.width < 600"
    grow
    color="blue"
  >
    <v-btn value="home" to="/">
      <span>Home</span>

      <v-icon>mdi-home</v-icon>
    </v-btn>

    <v-btn value="about" to="about">
      <span>About</span>

      <v-icon>mdi-human-greeting</v-icon>
    </v-btn>

    <v-btn value="workspace" to="workspace">
      <span>Workspace</span>

      <v-icon>mdi-folder-account</v-icon>
    </v-btn>
  </v-bottom-navigation>
</template>

<script>
export default {
  data: () => {
    return {
      value: "home",
    };
  },
};
</script>
