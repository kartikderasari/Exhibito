<template>
  <v-main class="half-bg">
    <v-container>
      <v-row>
        <v-card class="pa-8" outlined flat rounded>
          <v-container>
            <v-row>
              <v-card-title
                class="py-0 font-weight-medium headline teal--text text--darken-2"
              >
                About
              </v-card-title>
            </v-row>
            <v-row>
              <v-col cols="4" class="d-flex ">
                <v-img class="rounded-lg" src="../assets/new.jpg"> </v-img>
              </v-col>
              <v-col cols="8">
                <v-card-text class="pl-0 ml-0">
                  <h3
                    class="py-0 font-weight-medium title teal--text text--darken-2"
                  >
                    Some text Some text
                  </h3>
                  I’m a Final Year Computer Engineering Student passionate about
                  Developer Community Building & creating impacts through
                  building relationships, delivering Events and Community
                  Programs with Developer Advocacy. It has been about three
                  years since I started my journey around Communities & my
                  passion has always pushed me more to bring people together to
                  drive Advocacy and Adoption efficiencies. With this
                  enthusiasm, I have been leading a bunch of Communities for
                  Developers such as IEEE Student Branch, Google Developer
                  Student Club, Google Developers Group, and IEEE India Council
                  Industry Relations Team.
                </v-card-text>
                <v-card-actions> </v-card-actions>
              </v-col>
            </v-row>
          </v-container>
        </v-card>
      </v-row>
    </v-container>
  </v-main>
</template>

<style>
.half-bg {
  background: linear-gradient(
    to bottom,
    #e3f2fd 0%,
    #e3f2fd 50%,
    white 50%,
    white 100%
  );
}
</style>
