<template>
  <v-app>
    <presentation/>
  </v-app>
</template>

<script>
  import Presentation from "./../components/home/Presentation"

   export default {
    name: "Home",
     components: {
      Presentation
     },
     data() {
       return {
        
       }
     }
   };
</script>