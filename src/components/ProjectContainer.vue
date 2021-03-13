<template>
  <v-container>
    <v-card class="mx-auto px-8" color="transparent" flat>
      <v-row>
        <v-card-title
          class="py-0 pl-0 font-weight-medium headline teal--text text--darken-2"
        >
          Projects
        </v-card-title>
      </v-row>
      <v-row>
        <v-col>
          <v-slide-group v-model="model" class="" show-arrows="">
            <v-slide-item class="mb-10" v-for="n in 6" :key="n">
              <ProjectCard />
            </v-slide-item>
          </v-slide-group>
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
  }),
  components: { ProjectCard },
};
</script>
