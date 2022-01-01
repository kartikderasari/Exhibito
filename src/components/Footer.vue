<template>
  <v-footer  class="grey lighten-4">
    <v-container>
      <v-row no-gutters>
        <v-col
          class="text-center text-sm-center text-md-start text-lg-start"
          cols="12"
          sm="6"
          md="6"
          lg="6"
        >
          <span class="heading">
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
          <v-btn
            icon
            :href="'mailto:' + userData.email"
            target="_blank"
            rel="noreferrer noopener"
            aria-label="Mail"
          >
            <v-icon>mdi-email</v-icon>
          </v-btn>
          <v-btn
            icon
            :href="userData.Facebook"
            target="_blank"
            rel="noreferrer noopener"
            aria-label="Facebook"
          >
            <v-icon>mdi-facebook</v-icon>
          </v-btn>
          <v-btn
            icon
            :href="userData.Instagram"
            target="_blank"
            rel="noreferrer noopener"
            aria-label="Instagram"
          >
            <v-icon>mdi-instagram</v-icon>
          </v-btn>
          <v-btn
            icon
            :href="userData.LinkedIn"
            target="_blank"
            rel="noreferrer noopener"
            aria-label="LinkedIn"
          >
            <v-icon>mdi-linkedin</v-icon>
          </v-btn>
          <v-btn
            icon
            :href="userData.GitHub"
            target="_blank"
            rel="noreferrer noopener"
            aria-label="GitHub"
          >
            <v-icon>mdi-github</v-icon>
          </v-btn>
          <v-btn
            icon
            :href="userData.Twitter"
            target="_blank"
            rel="noreferrer noopener"
            aria-label="Twitter"
          >
            <v-icon>mdi-twitter</v-icon>
          </v-btn>
        </v-col>
        <v-col cols="12" class="text-center font-weight-medium text--secondary">
          <v-divider class="pb-2"></v-divider>
          <strong
          class="code-font"
            >© Created by
            <a
              class="text-decoration-none purple--text"
              href="https://github.com/kartikderasari/"
              target="_blank"
              rel="noreferrer noopener"
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
