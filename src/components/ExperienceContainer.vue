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
          class="pb-3 pl-0 font-weight-medium headline teal--text text--darken-2"
        >
          Experience
        </v-card-title>
      </v-row>
      <v-row>
        <v-col
          cols="12"
          sm="6"
          md="6"
          lg="4"
          v-for="(experience, index) in experiences"
          :key="index"
        >
          <ExperienceCard :experience="experience" />
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
import ExperienceCard from "@/components/ExperienceCard.vue";
import FDK from "@/config/firebase.js";
export default {
  data: () => {
    return {
      loading: false,
      experiences: null,
    };
  },
  components: { ExperienceCard },
  methods: {
    readExpData: function() {
      this.loading = true;
      this.experiences = [];
      FDK.firestore()
        .collection("experiences")
        .get()
        .then((doc) => {
          doc.forEach((doc) =>
            this.experiences.push({ id: doc.id, ...doc.data() })
          );
        })
        .then(() => (this.loading = false));
    },
  },
  created: function() {
    this.readExpData();
  },
};
</script>
