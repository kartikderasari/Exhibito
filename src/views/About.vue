<template>
  <v-container class="mt-15" style="position: relative; z-index:1" fluid>
    <v-row class="bg-overlay bg-overlay2">
      <v-container>
        <v-row align="center">
          <v-col class="my-15 pt-15" cols="9">
            <v-card flat color="transparent">
              <v-card-text class="py-0">
                Hello, I'm Kartik! <br />
                Talk to me about
              </v-card-text>
              <v-card-title class="py-0"
                >Web & Community Building!</v-card-title
              >
              <v-card-actions class="ml-2">
                <v-btn class="primary mr-2 my-2" small>About</v-btn>
                <v-btn class="text--blue my-2" outlined small
                  >Let's Connect</v-btn
                >
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
          <v-col cols="3">
            <v-img
              class="rounded-circle"
              src="@/assets/profile.jpg"
              width="230"
            >
            </v-img>
          </v-col>
        </v-row>
      </v-container>
    </v-row>
  </v-container>
</template>

<style>
.bg-overlay::before {
  content: "";
  background: url("../assets/Gradient_above.svg") no-repeat;
  background-size: 1500px 400px;
  position: absolute;
  top: 0px;
  left: 35%;
  width: 1500px;
  height: 400px;
  z-index: -2;
}

.bg-overlay2::after {
  content: "";
  background: url("../assets/Gradient_below.svg") no-repeat;
  background-size: 400px 200px;
  position: absolute;
  top: 300px;
  left: 0px;
  width: 400px;
  height: 200px;
  z-index: -2;
}
</style>
