<template>
  <v-toolbar 
    color="rgb(219, 214, 214, 0.3)" 
    flat 
    scroll-off-screen 
    app
  >
    <v-toolbar-side-icon class="white--text"/>
    <v-btn 
      class="white--text"
      flat
      to="/"
    >
      {{ applicationName }}
    </v-btn>
    <v-spacer/>
    <v-toolbar-items class="hidden-sm-and-down">
      <v-btn
        v-for="({ name, link }, i) in links"
        :key="i"
        :to="link"
        class="white--text"
        flat
      >
        {{ name }}
      </v-btn>
    </v-toolbar-items>
  </v-toolbar>
</template>

<script>
  export default {
    name: "MastHead",
    components: {
    
    },
    props: ['links'],
    data() {
      return {
        applicationName: "Intact Inside"    
      }
    }
  };
</script>