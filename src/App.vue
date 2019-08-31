<template>
  <v-app>
    <mast-head
      :links="links"/>
 
    <router-view />

    <mast-foot
      :links="links"/>
  </v-app>
</template>
 
<script>
  import MastHead from "./components/MastHead"
  import MastFoot from "./components/MastFoot"
 
  export default {
    name: "App",
    components: {
      MastHead,
      MastFoot
    },
    data() {
      return {
        links: 
          [
            {
              name: 'About',
              link: '#about'
            },
            {
              name: 'Music',
              link: '#music'
            },
            {
              name: 'Playlists',
              link: '#playlist'
            },
            {
              name: 'Contact',
              link: '#contact'
            }
          ]
      }
    }
  };
 </script>


<style>
  body {
    margin: 0;
    padding: 0;
  }
</style>
