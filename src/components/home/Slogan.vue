<template>
  <v-card color="rgba(255,255,255,0.99)">
    <!-- rgba(255,255,255,.5) -->
    <v-card-title>
      <v-icon large left>chevron_right</v-icon>
      <span class="font-weight-light display-1 black--text">Intact Inside</span>
    </v-card-title>
    <v-card-text class="headline justify-center black--text text-left">
      Every month is a new chance and a new hope! I hope you will enjoy my
      albums as much as I enjoyed releasing them.
    </v-card-text>
    <v-card-actions>
      <v-list-item class="grow">
        <v-list-item-avatar>
          <v-img class="elevation-6" src="./../../assets/PhilippeFournierAvatar.jpeg" />
        </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-title class="subtitle-1 black--text text-left">Philippe Fournier</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  name: "Slogan"
};
</script>

<style scoped>
.text-left {
  text-align: left;
}
</style>
