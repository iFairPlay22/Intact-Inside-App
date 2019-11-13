<template>
  <v-bottom-navigation
    app
    background-color="rgba(145,145,145,.1)"
    color="white"
    dark
    horizontal
  >
    <v-btn
      v-for="({ title, icon, link }, i) in items"
      :key="i"
      @click="redirect(link)"
    >
      <span class="subtitle-1">
        {{ title }}
      </span>
      <v-icon>
        {{ icon }}
      </v-icon>
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
          title: "Share",
          icon: "share",
          link: ""
        },
        {
          title: "Facebook",
          icon: "mdi-facebook",
          link: "https://www.facebook.com/insideintact/"
        },
        {
          title: "Youtube",
          icon: "mdi-youtube",
          link: "https://www.youtube.com/channel/UC2AtMri_kgObNgW2jH7iOFw/"
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
