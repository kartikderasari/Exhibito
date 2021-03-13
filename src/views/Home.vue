<template>
  <v-main>
    <HomeCard :userData="userData" />
  </v-main>
</template>

<script>
import HomeCard from "@/components/HomeCard.vue";

export default {
  components: { HomeCard },
  props: ["userData"],
};
</script>
