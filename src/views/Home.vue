<template>
  <HomeCard class="half-bg" :userData="userData" />
</template>

<script>
import HomeCard from "@/components/HomeCard.vue";

export default {
  components: { HomeCard },
  props: ["userData"],
};
</script>

<style>
.half-bg {
  background: linear-gradient(
    to right,
    #e6dace 0%,
    #e6dace 40%,
    white 40%,
    white 100%
  );
  height: 100%;
}
</style>