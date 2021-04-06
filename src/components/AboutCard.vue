<template>
  <v-container>
    <v-card class="py-10 px-8 rounded-lg" outlined flat rounded>
      <v-row>
        <v-card-title
          class="py-0 pl-0 font-weight-medium headline text--secondary"
        >
          About
        </v-card-title>
      </v-row>
      <v-row>
        <v-col cols="12" sm="12" md="12" lg="4" class="d-flex align-center">
          <v-img
            class="rounded-lg"
            src="https://raw.githubusercontent.com/kartikderasari/Portfolio-Assets/main/Profile/Cover-Image.svg?token=AJSPHONSK4ENTBWRBGVL2M3AK6VR4"
            lazy
          >
          </v-img>
        </v-col>
        <v-col cols="12" sm="12" md="12" lg="8">
          <v-card-text class="pl-0 ml-0">
            <h3
              class="py-0 font-weight-medium title text--secondary teal--text"
            >
              Hello, I'm {{ userData.name }}!
            </h3>
            {{ userData.about }}
          </v-card-text>
          <v-card-actions class="pl-0 py-0">
            <v-btn
              class="purple white--text px-2 px-sm-5 px-md-5 px-lg-5"
              to="workspace"
              >See Work</v-btn
            >
            <v-btn
              outlined
              color="purple"
              class="px-2 px-sm-5 px-md-5 px-lg-5"
              :href="'mailto:' + userData.email"
              >Contact
              <v-icon right> mdi-open-in-new </v-icon>
            </v-btn>
          </v-card-actions>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
export default {
  props: ["userData"],
};
</script>
