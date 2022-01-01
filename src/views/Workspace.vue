<template>
  <v-container fluid>
    <!-- <v-row>
      <v-col class="mx-auto" cols="12" md="12" sm="12" lg="10" xl="10">
        <BlogContainer :projects="projects" />
      </v-col>
    </v-row> -->
    <v-row class="grey lighten-4">
      <v-col class="mx-auto" cols="12" md="12" sm="12" lg="10" xl="10">
        <ProjectContainer :projects="projects" />
      </v-col>
    </v-row>
    <v-row>
      <v-col class="mx-auto" cols="12" md="12" sm="12" lg="10" xl="10">
        <VolunteeringContainer :volunteering="volunteering" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import VolunteeringContainer from "@/components/VolunteeringContainer.vue";
import ProjectContainer from "@/components/ProjectContainer.vue";
// import BlogContainer from "@/components/BlogContainer.vue";

export default {
  data: () => {
    return {
      show: false,
      model: 0,
    };
  },
  components: { VolunteeringContainer, ProjectContainer },
  props: ["volunteering", "projects"],
};
</script>

<style scoped>
.half-bg {
  background: linear-gradient(
    to bottom,
    white 0%,
    white 45%,
    #f5f5f5 45%,
    #f5f5f5 100%
  );
}
</style>
