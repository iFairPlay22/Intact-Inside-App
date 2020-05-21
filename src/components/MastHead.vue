<template>
  <v-app-bar
    app
    color="rgba(255,255,255,.025)"
    light
    dense
    prominent
    scroll-threshold="0"
    hide-on-scroll
  >
    <v-card height="100%" color="transparent">
      <v-card-title class="title white--text">Intact Inside</v-card-title>
    </v-card>
    <div class="flex-grow-1"></div>
    <v-btn icon v-for="({ icon, link }, i) in icons" :key="i" @click="redirect(link)">
      <v-icon class="white--text text--darken-1">{{ icon }}</v-icon>
      <!-- black -->
    </v-btn>
  </v-app-bar>
</template>

<script>
export default {
  name: "MastHead",
  data() {
    return {
      icons: [
        {
          icon: "mdi-instagram",
          link: "https://www.instagram.com/intactinside//"
        },
        {
          icon: "mdi-youtube",
          link: "https://www.youtube.com/channel/UC2AtMri_kgObNgW2jH7iOFw/"
        }
      ]
    };
  },
  methods: {
    redirect(link) {
      window.open(link, "_blank");
    }
  }
};
</script>
