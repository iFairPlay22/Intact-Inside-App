<template>
    <v-app id="content">
        <mast-head/>

        <router-view/>

        <mast-foot/>
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
              name: 'About Me',
              link: '#about'
            },
            {
              name: 'Last Songs',
              link: '#music'
            },
            {
              name: 'Albums',
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