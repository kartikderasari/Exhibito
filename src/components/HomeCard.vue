<template>
  <v-main>
    <v-container style="position: relative; z-index:1" fluid>
      <v-row :class="bgClass">
        <v-container>
          <v-row align="center">
            <v-col class="my-10 pt-10 pt-5" cols="12" lg="9" md="6" sm="12">
              <v-card flat color="transparent">
                <v-card-text class="py-0 title font-weight-normal">
                  Hello, I'm Kartik! <br />
                  Talk to me about
                </v-card-text>
                <v-card-title
                  class="py-0 font-weight-medium headline teal--text text--darken-2"
                >
                  <span style="border-bottom:6px solid #64B5F6;">
                    Web & Community Building!
                  </span>
                </v-card-title>
                <v-card-actions class="ml-2 mt-2">
                  <v-btn class="blue mr-2 white--text px-5">About</v-btn>
                  <v-btn class="blue--text px-5" outlined>Let's Connect</v-btn>
                </v-card-actions>
                <v-card-actions>
                  <v-btn icon>
                    <v-icon>mdi-email</v-icon>
                  </v-btn>
                  <v-btn icon>
                    <v-icon>mdi-facebook</v-icon>
                  </v-btn>
                  <v-btn icon>
                    <v-icon>mdi-instagram</v-icon>
                  </v-btn>
                  <v-btn icon>
                    <v-icon>mdi-linkedin</v-icon>
                  </v-btn>
                  <v-btn icon>
                    <v-icon>mdi-github</v-icon>
                  </v-btn>
                  <v-btn icon>
                    <v-icon>mdi-twitter</v-icon>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col cols="12" lg="3" md="6" sm="12">
              <v-img
                class="rounded-circle"
                src="@/assets/profile.jpg"
                max-width="250"
              >
              </v-img>
            </v-col>
          </v-row>
        </v-container>
      </v-row>
    </v-container>
  </v-main>
</template>

<style>
.bg-overlay::before {
  content: "";
  background: url("../assets/Gradient_above.svg") no-repeat;
  background-size: 130vw 65vh;
  position: absolute;
  top: -5vh;
  right: 0px;
  width: 84vw;
  height: 65vh;
  z-index: -2;
}

.bg-overlay2::after {
  content: "";
  background: url("../assets/gr_below.svg") no-repeat;
  background-size: 27vw 26vh;
  position: absolute;
  bottom: -18vh;
  left: 0px;
  width: 27vw;
  height: 26vh;
  z-index: -2;
}
</style>

<script>
export default {
  data: () => {
    return {
      bgClass: null,
    };
  },
  watch: {
    bgClass: function() {
      if (screen.width < 980) {
        this.bgClass = "";
      } else {
        this.bgClass = "bg-overlay bg-overlay2";
      }
    },
  },
};
</script>
