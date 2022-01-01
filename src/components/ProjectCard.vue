<template>
  <v-container fluid>
    <v-card
      class="d-flex flex-column"
      elevation="2"
      outlined
      min-height="400"
    >
      <v-row no-gutters>
        <v-col cols="12">
          <v-img
            class="rounded-t grey lighten-4"
            height="22vh"
            :src="project.projectImageURL"
            :lazy-src="project.projectImageURL"
            lazy
          ></v-img>

          <v-card-title>
            <span class="heading">
            {{ project.title }}
            </span>
          </v-card-title>

          <v-card-text v-if="project.brief.length < 120" class="text-justify">
            <span class="content">
            {{ project.brief }}
            </span>
          </v-card-text>
          <v-card-text v-else class="text-justify">
            <span class="content">
            {{ project.brief.slice(0, 180) }}...
            </span>
          </v-card-text>
        </v-col>

        <v-col class="d-flex flex-column justify-end" cols="12">
          <v-card-actions class="pl-4 d-flex flex-wrap">
            <v-chip class="mb-1 mr-1 lato-font" small>
              {{ project.techStack }}
            </v-chip>
          </v-card-actions>
          <v-divider class="mx-4"></v-divider>
          <v-card-actions class="pl-4 d-flex flex-wrap pb-3">
            <v-btn
              class="purple white--text"
              elevation="0"
              small
              target="_blank"
              :href="project.liveURL"
              rel="noreferrer noopener"
              aria-label="Project URL"
            >
              View Project
            </v-btn>
            <v-btn
              color="purple"
              text
              small
              target="_blank"
              :href="project.githubURL"
              rel="noreferrer noopener"
              aria-label="GitHub URL"
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
