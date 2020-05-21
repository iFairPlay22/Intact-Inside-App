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
    <v-btn v-for="({ title, icon, link }, i) in items" :key="i" @click="redirect(link)">
      <span class="subtitle-1 white--text">{{ title }}</span>
      <!-- black -->
      <v-icon class="white--text">{{ icon }}</v-icon>
      <!-- black -->
    </v-btn>
    <Law />
  </v-bottom-navigation>
</template>

<script>
import Law from "@/components/home/Law.vue";

export default {
  name: "MastFoot",
  components: { Law },
  data() {
    return {
      items: [
        {
          title: "Instagram",
          icon: "mdi-instagram",
          link: "https://www.instagram.com/intactinside/"
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
      window.open(link, "_blank");
    }
  }
};
</script>
