<template>
  <v-app-bar app color="white" elevate-on-scroll dense>
    <div class="headline text-no-wrap pt-1" style="width: 250px">
      <router-link
        class="font-weight-medium text--secondary text-decoration-none"
        to="/"
        style="width: 250px"
      >
        {{ userData.name }}
      </router-link>
    </div>

    <v-tabs right v-if="this.$vuetify.breakpoint.width > 600">
      <v-tab to="/">Home</v-tab>
      <v-tab to="about">About</v-tab>
      <v-tab to="workspace">Workspace</v-tab>
    </v-tabs>
  </v-app-bar>
</template>

<script>
export default {
  props: ["userData"],
};
</script>
