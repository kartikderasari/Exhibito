<template>
  <v-footer padless>
    <v-container>
      <v-card flat class="grey lighten-4">
        <v-card-title>
          <span class="title font-weight-medium grey--text text--darken-1">
            {{ userData.name }}
          </span>
          <v-spacer></v-spacer>
          <v-btn icon :href="'mailto:' + userData.email" target="_blank">
            <v-icon>mdi-email</v-icon>
          </v-btn>
          <v-btn icon :href="userData.Facebook" target="_blank">
            <v-icon>mdi-facebook</v-icon>
          </v-btn>
          <v-btn icon :href="userData.Instagram" target="_blank">
            <v-icon>mdi-instagram</v-icon>
          </v-btn>
          <v-btn icon :href="userData.LinkedIn" target="_blank">
            <v-icon>mdi-linkedin</v-icon>
          </v-btn>
          <v-btn icon :href="userData.GitHub" target="_blank">
            <v-icon>mdi-github</v-icon>
          </v-btn>
          <v-btn icon :href="userData.Twitter" target="_blank">
            <v-icon>mdi-twitter</v-icon>
          </v-btn>
        </v-card-title>
        <v-divider></v-divider>
        <v-card-text
          class="text-center font-weight-medium grey--text text--darken-1"
        >
          <strong
            >© Created by
            <a
              class="text-decoration-none"
              href="https://github.com/kartikderasari/"
              target="_blank"
              >Kartik Derasari</a
            ></strong
          >
        </v-card-text>
      </v-card>
    </v-container>
  </v-footer>
</template>

<script>
export default {
  props: ["userData"],
};
</script>
