<template>
  <div id="app">
    <mast-head
      :links="links"/>

    <router-view />

    <mast-foot
      :links="links"/>
  </div>
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
              link: 'home#about'
            },
            {
              name: 'Music',
              link: 'home#music'
            },
            {
              name: 'Playlists',
              link: 'home#playlist'
            },
            {
              name: 'Contact',
              link: 'home#contact'
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
