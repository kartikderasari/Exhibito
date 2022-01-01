<template>
  <v-app>
    <Navbar :userData="data.userInfo" v-if="!loading" />
    <v-main v-if="!loading" class="pb-0 mb-0">
      
        <router-view
          :userData="data.userInfo"
          :projects="data.projects"
          :experiences="data.experiences"
          :education="data.education"
          :techStack="data.techStack"
          :volunteering="data.volunteering"
        >
        </router-view>
      <!-- </v-scroll-y-reverse-transition> -->
    </v-main>
    <Footer
      :userData="data.userInfo"
      v-if="!loading && this.$route.path != '/'"
    />
    <BottomNav />
    <v-progress-circular
      class="mx-auto my-15 py-15"
      :size="50"
      color="primary"
      indeterminate
      v-if="loading"
    ></v-progress-circular>
  </v-app>
</template>

<script>
import Navbar from "@/components/Navbar";
import Footer from "@/components/Footer";
import BottomNav from "@/components/BottomNav";
import data from "./data/data.json";
export default {
  name: "App",
  components: { Navbar, Footer, BottomNav },
  data: () => ({
    data: data,
    userData: null,
    loading: false,
  }),
};
</script>

<style>
.scrollbar {
  margin-left: 30px;
  float: left;
  height: 300px;
  width: 65px;
  background: #f5f5f5;
  overflow-y: scroll;
  margin-bottom: 25px;
}
</style>
