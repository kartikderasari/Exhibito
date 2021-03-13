<template>
  <v-container fluid>
    <v-row class="half-bg">
      <v-col class="my-5" cols="12">
        <AboutCard :userData="userData" />
      </v-col>
    </v-row>
    <v-row>
      <v-col class="grey lighten-4 my-5" cols="12">
        <TechStack />
      </v-col>
    </v-row>
    <v-row>
      <v-col class="my-5" cols="12">
        <EducationTimeline />
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
.half-bg {
  background: linear-gradient(
    to bottom,
    #64b5f6 0%,
    #90caf9 50%,
    white 50%,
    white 100%
  );
}
</style>

<script>
import AboutCard from "@/components/AboutCard.vue";
import TechStack from "@/components/TechStack.vue";
import EducationTimeline from "@/components/EducationTimeline.vue";
export default {
  components: { AboutCard, TechStack, EducationTimeline },
  props: ["userData"],
};
</script>
