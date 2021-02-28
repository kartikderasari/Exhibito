<template>
  <v-container class="my-5">
    <v-card class="py-15 px-5 rounded-xl" outlined elevation="3">
      <v-row align="center" justify="center">
        <v-col cols="10" md="4" lg="4" sm="10" class="d-flex justify-center">
          <v-img
            class="rounded-circle"
            src="@/assets/profile.png"
            max-width="300"
            max-height="300"
          >
          </v-img>
        </v-col>
        <v-col cols="12" md="8" lg="8" sm="12">
          <v-card-title class="headline font-weight-medium teal--text">
            Hi, I'm Kartik Derasari!
          </v-card-title>
          <v-card-text class="body-1">
            I love exploring Web technologies while building appealing and
            interactive websites. Around these times, I'm indulged in
            experimenting JavaScript to make websites more lively. Meanwhile,
            I'm also exploring UI designing to enhance the web development
            experience.
          </v-card-text>
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
          <v-card-actions>
            <v-btn color="primary" elevation="0" text>Let's Connect</v-btn>
          </v-card-actions>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>
