<template>
  <v-bottom-navigation
    app
    background-color="rgba(255,255,255,.025)"
    color="black"
    dark
    horizontal
    scroll-threshold="0"
    hide-on-scroll
  >
    <v-btn
      v-for="({ title, icon, link }, i) in items"
      :key="i"
      @click="redirect(link)"
    >
      <span class="subtitle-1 white--text">{{ title }}</span> <!-- black -->
      <v-icon class="white--text">{{ icon }}</v-icon> <!-- black -->
    </v-btn>
  </v-bottom-navigation>
</template>

<script>
export default {
  name: "MastFoot",
  data() {
    return {
      items: [
        {
          title: "Facebook",
          icon: "mdi-facebook",
          link: "https://www.facebook.com/PhilippeFournierVoquer/"
        },
        {
          title: "Youtube",
          icon: "mdi-youtube",
          link: "https://www.youtube.com/channel/UC2AtMri_kgObNgW2jH7iOFw/"
        },
        {
          title: "Email",
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
