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
        <v-card-title
          class="font-weight-medium pl-0 headline teal--text text--darken-2"
          >Tech-Stack</v-card-title
        >
        <v-card-text class="d-flex justify-center align-center">
          <div v-for="(skill, index) in skills" :key="index">
            <v-img class="ma-2" :src="skill.skillLogoURL" width="4vw"></v-img>
          </div>
        </v-card-text>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
import FDK from "@/config/firebase.js";
export default {
  data: () => {
    return {
      skills: null,
      loading: false,
    };
  },
  methods: {
    readSkillsData: function() {
      this.loading = true;
      this.skills = [];
      FDK.firestore()
        .collection("skills")
        .get()
        .then((doc) => doc.forEach((doc) => this.skills.push(doc.data())))
        .then(() => (this.loading = false));
    },
  },
  mounted: function() {
    this.readSkillsData();
  },
};
</script>
