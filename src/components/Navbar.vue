<template>
  <v-app-bar app color="white" flat dense>
    <div class="headline text-no-wrap pt-1" style="width: 250px;">
      <router-link
        class="font-weight-medium teal--text text-decoration-none"
        to="/"
        style="width: 250px;"
      >
        Kartik Derasari
      </router-link>
    </div>

    <v-tabs right>
      <v-tab to="/">Home</v-tab>
      <v-tab to="about">About</v-tab>
      <v-tab to="resume">Resume</v-tab>
      <v-tab to="work">Work</v-tab>
      <v-tab to="contact">Contact</v-tab>
    </v-tabs>
  </v-app-bar>
</template>
