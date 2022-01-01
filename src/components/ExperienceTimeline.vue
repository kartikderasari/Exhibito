<template>
  <v-container>
    <v-card flat class="py-5" color="transparent">
      <v-row>
        <v-card-title class="pl-8 font-weight-medium headline text--secondary">
          Experience
        </v-card-title>
      </v-row>
      <v-row>
        <v-timeline class="pt-0 mt-4 mx-auto" align-top dense>
          <v-timeline-item
            small
            v-for="(exp, index) in experiences"
            :key="index"
          >
            <v-card max-width="900" elevation="8">
              <v-row class="pa-2 d-flex align-center" no-gutters>
                <v-col
                  v-if="width > 690"
                  cols="2"
                  class="d-flex justify-center"
                >
                  <v-img
                    class="rounded-circle"
                    :lazy-src="exp.companyLogoURL"
                    :src="exp.companyLogoURL"
                    max-width="100"
                  ></v-img>
                </v-col>
                <v-col cols="12" sm="10" md="10" lg="10">
                  <v-card-title class="flex-column align-start py-2">
                    <div class="heading">
                      {{ exp.designation }}, {{ exp.companyName }}
                    </div>
                    <small class="lato-font grey-text">{{ exp.start }} - {{ exp.end }}</small>
                  </v-card-title>
                </v-col>
              </v-row>

              <v-card-text v-if="exp.brief" class="pt-3 content text-justify" v-html="exp.brief">
              </v-card-text>
            </v-card>
          </v-timeline-item>
        </v-timeline>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
export default {
  computed: {
    width() {
      return this.$vuetify.breakpoint.width;
    },
  },
  props: ["experiences"],
};
</script>
