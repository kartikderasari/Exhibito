<template>
  <v-footer padless app absolute class="grey lighten-4">
    <v-container>
      <v-row no-gutters>
        <v-col
          class="text-center text-sm-center text-md-start text-lg-start"
          cols="12"
          sm="6"
          md="6"
          lg="6"
        >
          <span class="title font-weight-medium grey--text text--darken-1">
            {{ userData.name }}
          </span>
        </v-col>
        <v-col
          class="text-center text-sm-center text-md-end text-lg-end"
          cols="12"
          sm="6"
          md="6"
          lg="6"
        >
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
        </v-col>
        <v-col
          cols="12"
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
        </v-col>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script>
export default {
  props: ["userData"],
};
</script>
