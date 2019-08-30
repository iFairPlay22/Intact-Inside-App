<template>
  <div>
    <presentation/>
    <best-titles/>
    <last-album/>
    <albums/>
    <!-- <playlist/> -->
  </div>
</template>

<script>
  import Presentation from "./../components/home/Presentation"
  import BestTitles from "./../components/home/BestTitles"
  import LastAlbum from "./../components/home/LastAlbum"
  import Albums from "./../components/home/Albums"
  // import Playlist from "./../components/home/Playlist"

  export default {
    name: "home",
    components: {
      Presentation,
      BestTitles,
      LastAlbum,
      Albums,
      // Playlist
    },
    data() {
      return {
        title: "Intact-Inside"
      }
    }
  };
</script>
