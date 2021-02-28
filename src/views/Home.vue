<template>
  <v-lazy>
    <v-container fluid>
      <v-row class="py-15 half-bg">
        <HomeCard />
      </v-row>
    </v-container>
  </v-lazy>
</template>

<script>
import HomeCard from "@/components/HomeCard.vue";
export default {
  components: { HomeCard },
};
</script>

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
