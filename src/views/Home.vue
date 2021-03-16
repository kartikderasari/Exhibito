<template>
  <HomeCard :userData="userData" />
</template>

<script>
import HomeCard from "@/components/HomeCard.vue";

export default {
  components: { HomeCard },
  props: ["userData"],
};
</script>
