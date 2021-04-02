<template>
  <v-container>
    <v-card class="mx-auto" color="transparent" flat>
      <v-row>
        <v-card-title
          class="py-0 pl-8 font-weight-medium headline text--secondary"
        >
          Projects
        </v-card-title>
      </v-row>
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
        <v-col>
          <v-slide-group v-model="model" show-arrows mandatory>
            <v-slide-item
              class="mb-10 pl-3"
              v-for="(project, index) in projects"
              :key="index"
            >
              <ProjectCard :project="project" />
            </v-slide-item>
          </v-slide-group>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
import ProjectCard from "@/components/ProjectCard.vue";
import FDK from "@/config/firebase.js";
export default {
  data: () => ({
    model: null,
    projects: null,
    loading: false,
  }),
  components: { ProjectCard },
  methods: {
    readProjectData: function () {
      this.loading = true;
      this.projects = [];
      FDK.firestore()
        .collection("projects")
        .get()
        .then((doc) => {
          doc.forEach((doc) => this.projects.push(doc.data()));
        })
        .then(() => (this.loading = false));
    },
  },
  created: function () {
    this.readProjectData();
  },
};
</script>
