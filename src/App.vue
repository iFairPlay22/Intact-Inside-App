<template>
  <v-app class="background-image">
    <mast-head />

    <router-view />

    <mast-foot />
  </v-app>
</template>

<script>
import MastHead from "./components/MastHead";
import MastFoot from "./components/MastFoot";

export default {
  name: "App",
  components: {
    MastHead,
    MastFoot
  },
  data() {
    return {
      links: [
        {
          name: "About Me",
          link: "#about"
        },
        {
          name: "Last Songs",
          link: "#music"
        },
        {
          name: "Albums",
          link: "#playlist"
        },
        {
          name: "Contact",
          link: "#contact"
        }
      ]
    };
  }
};
</script scoped>

<style>
/* width */
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: transparent;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: rgba(145, 145, 145, 0.4);
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: rgba(145, 145, 145, 0.6);
}

.background-image {
  background-image: url("assets/Carousel/5.jpg") !important;
  background-size: cover !important;
  background-repeat: no-repeat !important;
}
</style>
