<template>
  <v-container fluid>
    <v-row>
      <v-col class="grey lighten-4" cols="12">
        <ExperienceContainer />
      </v-col>
    </v-row>
    <v-row>
      <v-col class="half-bg my-16" cols="12">
        <ProjectContainer />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import ExperienceContainer from "@/components/ExperienceContainer.vue";
import ProjectContainer from "@/components/ProjectContainer.vue";

export default {
  data: () => {
    return {
      show: false,
      model: 0,
    };
  },
  components: { ExperienceContainer, ProjectContainer },
  methods: {},
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
