<template>
  <v-container>
    <v-card class="mx-3 mt-5" max-width="280" elevation="5">
      <v-img
        height="150"
        src="https://wallpapercave.com/wp/qr0bJYf.jpg"
      ></v-img>

      <v-card-title class="pb-0"> {{ project.title }} </v-card-title>

      <v-card-text>
        {{ project.brief }}
      </v-card-text>
      <v-row>
        <v-col>
          <v-card-actions class="pl-4">
            <v-chip small> {{ project.techStack }} </v-chip>
          </v-card-actions>
          <v-divider class="mx-4"></v-divider>
          <v-card-actions class="pl-4">
            <v-btn
              class="blue white--text"
              small
              target="_blank"
              :href="project.liveURL"
            >
              View Project
            </v-btn>
            <v-btn
              color="blue"
              text
              small
              target="_blank"
              :href="project.githubURL"
            >
              View Code
            </v-btn>
          </v-card-actions>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
export default {
  props: ["project"],
};
</script>
