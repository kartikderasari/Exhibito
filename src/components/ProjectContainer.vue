<template>
  <v-container class="py-8">
    <v-row>
      <v-card-title
        class="pt-5 pl-8 font-weight-medium headline text--secondary"
      >
        Projects
      </v-card-title>
    </v-row>
    <v-card class="py-5 px-8" color="transparent" flat>
      <v-row v-if="loading">
        <v-progress-circular
          class="mx-auto my-10"
          :size="40"
          color="primary"
          indeterminate
          v-if="loading"
        ></v-progress-circular>
      </v-row>
      <v-row v-if="!loading">
        <v-col
          cols="12"
          sm="6"
          md="6"
          lg="4"
          v-for="(project, index) in projects"
          :key="index"
        >
          <ProjectCard :project="project" />
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
import ProjectCard from "@/components/ProjectCard.vue";

export default {
  data: () => ({
    model: null,
    projects: null,
    loading: false,
  }),
  components: { ProjectCard },
  props: ["projects"],
};
</script>
