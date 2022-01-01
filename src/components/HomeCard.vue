<template>
  <v-scroll-y-reverse-transition mode="out-in">
    <v-container fluid class="d-flex">
      <v-row>
        <v-col class="my-auto" cols="10" lg="6" md="6" sm="6" xl="6">
          <v-col class="d-flex justify-end">
            <v-card
              class="my-12 pa-8 py-12"
              width="400"
              elevation="5"
              color="#F4ECE6"
            >
              <v-img
                width="200"
                class="rounded-circle mx-auto mb-8 elevation-5"
                :src="userData.profilePhotoURL"
              ></v-img>

              <v-card-title>
                <span
                  class="text-center mx-auto acme-font"
                  style="
                    font-size: 2.5rem;
                    font-weight: 500;
                    line-height: 40px;
                    color: #666666;
                  "
                >
                  Kartik
                  Derasari
                </span>
              </v-card-title>

              <!-- <v-divider inset class="mx-15 my-0"></v-divider> -->

              <v-card-text class="text-center">
                <span
                class="code-font"
                  style="
                    font-size: 1.2rem;
                    font-weight: bold;
                  "
                >
                  Full-Stack Developer
                </span>
              </v-card-text>

              <v-card-actions class="d-flex justify-center pa-0 ma-0 mt-5">
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
            </v-card>
          </v-col>
        </v-col>
        <v-col
          class="d-flex flex-wrap align-center"
          cols="11"
          xl="6"
          lg="6"
          md="6"
          sm="8"
        >
          <v-card flat color="transparent">
            <v-card-text class="py-0">
              <span class="font-weight-medium acme-font" style="font-size: 2rem; line-height: 40px;">
                Hello, I'm {{ userData.name }}! <br />
                Talk to me about
              </span>
            </v-card-text>
            <v-card-title
              class="
                py-0
                font-weight-medium
                text--secondary text--darken-2
                
              "
            >
              <span
                class="text-truncate font-weight-medium acme-font"
                style="border-bottom: 6px solid #64b5f6; font-size: 2rem; line-height: 40px;"
              >
                Web & Community Building!
              </span>
            </v-card-title>
            <v-card-text
              class="py-2"
              style="max-width: 700px; text-align: justify;"
            >
            <span class="content">
              {{ userData.shortBio }}
            </span>
            </v-card-text>
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
      </v-row>
    </v-container>
  </v-scroll-y-reverse-transition>
</template>


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