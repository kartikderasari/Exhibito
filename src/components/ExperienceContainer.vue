<template>
  <v-container>
    <v-card class="py-10 px-8" flat color="transparent">
      <v-row>
        <v-card-title
          class="pb-3 pl-0 font-weight-medium headline teal--text text--darken-2"
        >
          Experience
        </v-card-title>
      </v-row>
      <v-row>
        <v-col cols="4" v-for="n in 3" :key="n">
          <ExperienceCard />
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
import ExperienceCard from "@/components/ExperienceCard.vue";
export default {
  components: { ExperienceCard },
};
</script>
