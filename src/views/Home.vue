<template>
  <!-- <v-card height="100%" color="red" class="d-flex flex-column justify-center align-center">
    <slogan />
    <albums />
  </v-card>-->
  <v-card flat color="transparent" height="100%" class="d-flex justify-center align-center">
    <v-container fluid>
      <v-row>
        <v-col lg="5" offset-lg="1" md="6" offset-md="1" sm="12">
          <v-img contain src="@/assets/background.jpg" />
        </v-col>
        <v-col align-self="center" lg="4" offset-lg="1" md="4" offset-md="0" sm="10" offset-sm="1">
          <!-- <slogan /> -->
          <albums />
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>

<script>
// import Slogan from "./../components/home/Slogan";
import Albums from "./../components/home/Albums";

export default {
  name: "Home",
  components: {
    // Slogan,
    Albums
  }
};
</script>
