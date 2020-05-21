<template>
  <v-app class="background-image">
    <mast-head />
    <v-content>
      <router-view />
    </v-content>
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
</script>

<style scoped>
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

@media (min-width: 1000px) {
  .background-image {
    /* background-image: url("assets/background.jpg") !important; */
    /* background-size: cover !important; */
    /* background-repeat: no-repeat !important; */

    /* background-color: black !important; */

    background-image: linear-gradient(
      to right top,
      #000000,
      #000000,
      #000000,
      #000000,
      #000000,
      #000000,
      #000000,
      #000000,
      #7e76a8,
      rgb(134, 170, 239)
    ) !important;

    /* background-image: linear-gradient(
      to right top,
      #000000,
      #000000,
      #000000,
      #000000,
      #000000,
      #000000,
      #000000,
      #a95c2c,
      #dca50c
    ) !important; */
  }
}

@media (max-width: 1000px) {
  .background-image {
    background-color: black !important;
  }
}
</style>
