<template>
  <v-container>
    <v-row v-if="loading">
      <v-progress-circular
        class="mx-auto my-10"
        :size="40"
        color="primary"
        indeterminate
      ></v-progress-circular>
    </v-row>
    <v-card class="py-10 px-8" flat color="transparent" v-if="!loading">
      <v-row>
        <v-card-title
          class="pb-3 pl-0 font-weight-medium headline text--secondary"
        >
          Leadership and Volunteering
        </v-card-title>
      </v-row>
      <v-row>
        <v-col
          cols="12"
          sm="6"
          md="6"
          lg="4"
          v-for="(vtr, index) in volunteering"
          :key="index"
        >
          <VolunteeringCard :volunteering="vtr" />
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
import VolunteeringCard from "@/components/VolunteeringCard.vue";
export default {
  data: () => {
    return {
      loading: false,
    };
  },
  components: { VolunteeringCard },
  props: ["volunteering"],
};
</script>
