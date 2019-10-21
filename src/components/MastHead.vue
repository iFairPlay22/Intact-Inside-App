<template>
  <v-app-bar 
    absolute 
    color="rgba(145,145,145,.1)" 
    dark 
    dense
    prominent>
      <v-app-bar-nav-icon/>
      <v-toolbar-title class="text-center mb-1 headline">
          Intact Inside
      </v-toolbar-title>
      <div class="flex-grow-1"></div>
      <v-btn icon
        v-for="({icon, link}, i) in icons"
        :key="i"  
        @click="redirect(link)"
      >
        <v-icon>
          {{ icon }}
        </v-icon>
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
            icon: "share",
            link: ""
          },
          {
            icon: "mdi-facebook",
            link: "https://www.facebook.com/insideintact/"
          },
          {
            icon: "mdi-youtube",
            link: "https://www.youtube.com/channel/UC2AtMri_kgObNgW2jH7iOFw/"
          }
        ]
      }
    },
    methods: {
      redirect(link) {
        if (link !== "") {
          window.open(link, '_blank');
        } else {
          window.location.href = "mailto:intact.inside@gmail.com";
        }
      }
    }
  };
</script>