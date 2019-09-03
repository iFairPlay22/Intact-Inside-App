<template>
  <v-app>
    <presentation/>
    <best-titles/>
    <last-album/>
    <albums/>
    <!-- <playlist/> -->
    </v-app>
</template>

<script>
  import Presentation from "./../components/home/Presentation"
  import BestTitles from "./../components/home/BestTitles"
  import LastAlbum from "./../components/home/LastAlbum"
  import Albums from "./../components/home/Albums"
  // import Playlist from "./components/home/Playlist"

   export default {
    name: "Home",
     components: {
      Presentation,
      BestTitles,
      LastAlbum,
      Albums,
      // Playlist
     },
     data() {
       return {
        
       }
     }
   };
</script>