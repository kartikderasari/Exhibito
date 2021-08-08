<template>
  <v-container fluid>
    <v-row class="half-bg">
      <v-col class="my-5" cols="12">
        <AboutCard :userData="userData" />
      </v-col>
    </v-row>
    <v-row>
      <v-col class="grey lighten-4 my-5" cols="12">
        <ExperienceTimeline :experiences="experiences" />
      </v-col>
    </v-row>
    <v-row>
      <v-col class="my-5" cols="12">
        <TechStack :techStack="techStack" />
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
.half-bg {
  background: linear-gradient(
    to bottom,
    #f5f5f5 0%,
    #f5f5f5 50%,
    white 50%,
    white 100%
  );
}
</style>

<script>
import AboutCard from "@/components/AboutCard.vue";
import TechStack from "@/components/TechStack.vue";
// import EducationTimeline from "@/components/EducationTimeline.vue";
// import ExperienceContainer from "@/components/ExperienceContainer.vue";
import ExperienceTimeline from "@/components/ExperienceTimeline.vue";
export default {
  components: {
    AboutCard,
    TechStack,
    // EducationTimeline,
    // ExperienceContainer,
    ExperienceTimeline,
  },
  props: ["userData", "techStack", "education", "experiences"],
};
</script>
