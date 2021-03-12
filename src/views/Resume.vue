<template>
  <v-container fluid>
    <v-row>
      <v-col class="grey lighten-4" cols="12">
        <ExperienceContainer />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import ExperienceContainer from "@/components/ExperienceContainer.vue";
export default {
  data: () => {
    return {
      show: false,
    };
  },
  components: { ExperienceContainer },
};
</script>
