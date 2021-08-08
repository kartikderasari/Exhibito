<template>
  <v-container fluid>
    <v-row>
      <v-col class="grey lighten-4" cols="12">
        <VolunteeringContainer :volunteering="volunteering" />
      </v-col>
    </v-row>
    <v-row no-gutters>
      <v-col class="my-16" cols="12">
        <ProjectContainer :projects="projects" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import VolunteeringContainer from "@/components/VolunteeringContainer.vue";
import ProjectContainer from "@/components/ProjectContainer.vue";

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
