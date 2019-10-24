<template>
    <v-carousel height="100%" width="100%" hide-delimiters interval="1000">
        <v-carousel-item v-for="(link, i) in links" :key="i" :src="link">
            <v-container grid-list-md class="container">
                <v-layout align-center justify-center space-around column fill-height>
                    <slogan/>
                    <albums/>
                    <!--
                        <blog/>
                    -->
                </v-layout>
            </v-container>
        </v-carousel-item>
    </v-carousel>
</template>

<script>
  import Slogan from "./Slogan"
  import Albums from "./Albums"
  //import Blog from "./Blog"

  export default {
    name: "Presentation",
    components: {
        Slogan,
        Albums
        //Blog
    },
    data() {
      return {
        links: [
          require('../../assets/Carousel/1.jpg'),
          require('../../assets/Carousel/2.jpg'),
          require('../../assets/Carousel/3.jpg'),
          require('../../assets/Carousel/4.jpg'),
          require('../../assets/Carousel/5.jpg')
        ]
      }
    }
  };
</script>

<style scoped>
  .container {
    margin-top: 200px;
    margin-bottom: 200px;
  }
</style>