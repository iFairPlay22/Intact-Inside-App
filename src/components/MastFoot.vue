<template>
    <v-bottom-navigation
      absolute
      background-color="rgba(145,145,145,.1)" 
      color="black"
      dark
      horizontal
  >
    <v-btn>
      <span>Like</span>
      <v-icon>mdi-heart</v-icon>
    </v-btn>

    <v-btn>
      <span>Share</span>
      <v-icon>share</v-icon>
    </v-btn>

    <v-btn>
      <span>Contact us</span>
      <v-icon>create</v-icon>
    </v-btn>
  </v-bottom-navigation>
</template>

<script>
    export default {
        name: 'MastFoot',
        data () {
            return {
                
            }
        }
    }
</script>