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
    <div class="flex-grow-1"></div>
    <v-btn
      icon
      v-for="({ icon, link }, i) in icons"
      :key="i"
      @click="redirect(link)"
    >
      <v-icon class="black--text text--darken-1">{{ icon }}</v-icon>
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
          icon: "mdi-facebook",
          link: "https://www.facebook.com/PhilippeFournierVoquer/"
        },
        {
          icon: "mdi-youtube",
          link: "https://www.youtube.com/channel/UC2AtMri_kgObNgW2jH7iOFw/"
        },
        {
          icon: "mdi-email",
          link: ""
        }
      ]
    };
  },
  methods: {
    redirect(link) {
      if (link !== "") {
        window.open(link, "_blank");
      } else {
        window.location.href = "mailto:intact.inside@gmail.com";
      }
    }
  }
};
</script>
