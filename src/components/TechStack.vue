<template>
  <v-container>
    <v-row>
      <v-progress-circular
        class="mx-auto my-10"
        :size="40"
        color="primary"
        indeterminate
        v-if="loading"
      ></v-progress-circular>
    </v-row>
    <v-card class="py-5 px-8" color="transparent" flat v-if="!loading">
      <v-row>
        <v-card-title class="font-weight-medium pl-0 headline text--secondary"
          >Tech-Stack</v-card-title
        >
        <v-card-text class="d-flex justify-center flex-wrap align-end text-center">
          <div v-for="(skill, index) in techStack" :key="index">
            <v-tooltip bottom>
              <template v-slot:activator="{ on, attrs }">
                <v-img
                  class="mx-8 my-5"
                  :src="skill.skillLogoURL"
                  :lazy-src="skill.skillLogoURL"
                  width="5vw"
                  height="auto"
                  lazy
                  v-bind="attrs"
                  v-on="on"
                ></v-img>
                <span class="code-font" style="font-size: 1rem">{{ skill.skill }}</span>
              </template>
              <span class="code-font">{{ skill.skill }}</span>
            </v-tooltip>
          </div>
        </v-card-text>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
export default {
  data: () => {
    return {
      skills: null,
      loading: false,
    };
  },
  props: ["techStack"],
};
</script>
