<template>
        <v-app-bar 
          absolute 
          color="rgba(145,145,145,.1)" 
          dark 
          dense
          prominent>
            <v-app-bar-nav-icon/>
            <v-toolbar-title class="text-center mb-1">
                Intact Inside
            </v-toolbar-title>
            <div class="flex-grow-1"></div>
            <v-btn icon>
                <v-icon>mdi-heart</v-icon>
            </v-btn>
            <v-btn icon>
                <v-icon>share</v-icon>
            </v-btn>
            <v-btn icon>
                <v-icon>create</v-icon>
            </v-btn>
        </v-app-bar>
</template>

<script>
  export default {
    name: "MastHead",
    data() {
      return {
        
      }
    }
  };
</script>