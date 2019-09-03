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
          ],
        window: {
          width: 0,
          height: 0
        }
      }
    },
    created() {
      window.addEventListener('resize', this.handleResize)
      this.handleResize();
    },
    destroyed() {
      window.removeEventListener('resize', this.handleResize)
    },
    methods: {
      handleResize() {
        this.window.width = window.innerWidth;
        this.window.height = window.innerHeight;
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
