<template>
  <v-container>
    <v-card class="px-8" flat>
      <v-row>
        <v-card-title
          class="pl-0 font-weight-medium headline teal--text text--darken-2"
        >
          Education
        </v-card-title>
      </v-row>
      <v-row>
        <v-col>
          <v-timeline dense align-top>
            <v-timeline-item small color="blue" v-for="n in 3" :key="n">
              <v-card-title class="h4 pa-0">Computer Engineering</v-card-title>
              <v-card-text class="ma-0 pa-0">
                Silver Oak College of Engineering and Technology
              </v-card-text>
              <small>2017 - Present</small>
            </v-timeline-item>
          </v-timeline>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>
