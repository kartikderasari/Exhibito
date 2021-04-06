<template>
  <v-container fluid>
    <v-row
      class="mt-15 mb-15 mb-sm-15 mb-md-15 mb-lg-15 bg-overlay bg-overlay2"
      style="position: relative; z-index: 1"
    >
      <v-container class="mt-0 mt-lg-5 mt-md-10">
        <v-row align="center">
          <v-col
            class="my-lg-10 my-md-10 pt-10 pt-15 mx-sm-auto mx-md-start mx-lg-start mx-auto"
            cols="11"
            xl="8"
            lg="8"
            md="6"
            sm="8"
            order="2"
            order-sm="2"
            order-md="1"
            order-lg="1"
          >
            <v-card flat color="transparent">
              <v-card-text
                class="py-0 title text--secondary font-weight-normal"
              >
                Hello, I'm {{ userData.name }}! <br />
                Talk to me about
              </v-card-text>
              <v-card-title
                class="py-0 font-weight-medium headline text--secondary text--darken-2"
              >
                <span
                  class="text-truncate"
                  style="border-bottom: 6px solid #64b5f6"
                >
                  Web & Community Building!
                </span>
              </v-card-title>
              <v-card-text
                class="pb-0 pt-2 font-weight-medium subtitle-2"
                style="max-width: 700px"
              >
                {{ userData.shortBio }}
              </v-card-text>
              <v-card-actions class="d-flex align-center py-0">
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
              </v-card-actions>
              <v-card-actions class="ml-2">
                <v-btn
                  class="blue mr-2 white--text px-2 px-sm-5 px-md-5 px-lg-5"
                  to="/about"
                  >About</v-btn
                >
                <v-btn
                  class="blue--text px-2 px-sm-5 px-md-5 px-lg-5"
                  outlined
                  to="/workspace"
                  >See work</v-btn
                >
              </v-card-actions>
            </v-card>
          </v-col>
          <v-col
            class="mx-sm-auto mx-md-start mx-lg-start mx-auto"
            cols="10"
            lg="3"
            md="6"
            sm="6"
            order="1"
            order-sm="1"
            order-md="2"
            order-lg="2"
          >
            <v-img
              class="rounded-circle"
              :src="userData.profilePhotoURL"
              max-width="250"
              height="auto"
            >
            </v-img>
          </v-col>
        </v-row>
      </v-container>
    </v-row>
  </v-container>
</template>

<style>
.bg-overlay::before {
  content: "";
  background: url("../assets/gr_above.svg") no-repeat;
  background-size: 130vw 65vh;
  position: absolute;
  top: -5vh;
  right: 0px;
  width: 84vw;
  height: 65vh;
  z-index: -2;
}

.bg-overlay2::after {
  content: "";
  background: url("../assets/gr_below.svg") no-repeat;
  background-size: 27vw 13vw;
  position: absolute;
  bottom: -12vw;
  left: 0px;
  width: 27vw;
  height: 13vw;
  z-index: -2;
}
</style>

<script>
export default {
  data: () => {
    return {
      bgClass: null,
      loading: false,
    };
  },
  props: ["userData"],
};
</script>
