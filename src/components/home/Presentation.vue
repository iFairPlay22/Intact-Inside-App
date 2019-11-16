<template>
  <v-container grid-list-md class="container">
    <v-layout align-center justify-center space-around column fill-height>
      <slogan />
      <albums />
    </v-layout>
  </v-container>
</template>

<script>
import Slogan from "./Slogan";
import Albums from "./Albums";

export default {
  name: "Presentation",
  components: {
    Slogan,
    Albums
  }
};
</script>

<style scoped>
.container {
  margin-top: 50px;
  margin-bottom: 50px;
}
</style>
