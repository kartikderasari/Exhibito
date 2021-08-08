<template>
  <v-dialog v-model="dialog" width="700" retain-focus>
    <template v-slot:activator="{ on, attrs }">
      <v-card
        class="rounded-lg"
        outlined
        flat
        v-bind="attrs"
        v-on="on"
        height="150"
      >
        <v-card-text>
          <v-row class="my-auto" justify="center">
            <v-col cols="4" align="center">
              <v-img
                class="rounded-xl"
                :src="volunteering.companyLogoURL"
                max-width="120"
                max-height="120"
                lazy
              ></v-img>
            </v-col>
            <v-col cols="8" class="d-flex flex-column justify-center">
              <h5 class="title text-truncate">
                {{ volunteering.designation }}
              </h5>
              <p class="my-0 text-truncate">{{ volunteering.companyName }}</p>
              <p class="my-0">
                {{ volunteering.start }} - {{ volunteering.end }}
              </p>
            </v-col>
          </v-row>
        </v-card-text>
      </v-card>
    </template>

    <v-card>
      <v-card-text>
        <v-row class="d-flex align-center pt-4">
          <v-col cols="3" align="center">
            <v-img
              class="rounded-lg"
              :src="volunteering.companyLogoURL"
              max-width="120"
              max-height="120"
            ></v-img>
          </v-col>
          <v-col cols="9" class="">
            <h5 class="title">
              {{ volunteering.designation }}
            </h5>
            <p class="my-0">{{ volunteering.companyName }}</p>
            <p class="my-0">
              {{ volunteering.start }} - {{ volunteering.end }}
            </p>
          </v-col>
        </v-row>
      </v-card-text>

      <v-card-text>
        {{ volunteering.brief }}
      </v-card-text>

      <v-divider></v-divider>

      <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn
          color="primary"
          outlined
          :href="volunteering.companyWebsiteURL"
          target="_blank"
        >
          Learn More
        </v-btn>
        <v-btn color="primary" text @click="dialog = false"> Close </v-btn>
      </v-card-actions>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  data: () => {
    return {
      dialog: false,
    };
  },
  props: ["volunteering"],
};
</script>

<style scoped>
.v-card--link:focus:before {
  opacity: 0;
}
</style>
