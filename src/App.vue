<template>
  <v-app>
    <Navbar :userData="userData" v-if="!loading" />
    <v-main v-if="!loading">
      <v-divider></v-divider>
      <router-view :userData="userData"> </router-view>
    </v-main>
    <Footer :userData="userData" v-if="!loading" />
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
import FDK from "@/config/firebase.js";
import BottomNav from "@/components/BottomNav";
export default {
  name: "App",
  components: { Navbar, Footer, BottomNav },
  data: () => ({
    userData: null,
    loading: false,
  }),
  methods: {
    readUserInfoData: function() {
      this.loading = true;
      FDK.firestore()
        .collection("userInfo")
        .doc("data")
        .get()
        .then((doc) => (this.userData = doc.data()))
        .then(() => (this.loading = false));
    },
  },
  created: function() {
    this.readUserInfoData();
  },
};
</script>
