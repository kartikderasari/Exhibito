<template>
  <v-dialog id="ddialog" v-model="dialog" width="500" retain-focus>
    <template v-slot:activator="{ on, attrs }">
      <v-card class="rounded-xl" id="ad" outlined flat v-bind="attrs" v-on="on">
        <v-card-text>
          <v-row class="pa-2" justify="center">
            <v-col cols="4" align="center">
              <v-img
                class="rounded-lg"
                src="https://vrijraj.xyz/img/bootstrap.ffded238.svg"
                max-width="80"
                max-height="80"
              ></v-img>
            </v-col>
            <v-col cols="8" class="d-flex flex-column  justify-center">
              <h5 class="title">Designation</h5>
              <p class="my-0">Company Name</p>
              <p class="my-0">2019 - Present</p>
            </v-col>
          </v-row>
        </v-card-text>
      </v-card>
    </template>

    <v-card>
      <v-card-title class="headline grey lighten-2">
        Privacy Policy
      </v-card-title>

      <v-card-text>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
        velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
        occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
      </v-card-text>

      <v-divider></v-divider>

      <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn color="primary" text @click="dialog = false">
          I accept
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  data: () => {
    return {
      dialog: false,
    };
  },
};
</script>

<style scoped>
.v-card--link:focus:before {
  opacity: 0;
}
</style>
