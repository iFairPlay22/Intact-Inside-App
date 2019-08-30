<template>
    <header id="nav">
      <router-link 
        v-for="({name, link}, i) in links"
        :key="i"
        :to="link"
      >
        {{ name }}
      </router-link>
    </header>
</template>

<script>
  export default {
    name: "MastHead",
    components: {
      
    },
    props: ['links'],
    data() {
      return {
        
      }
    }
  };
</script>


<style>
  #nav {
    padding: 15px 0;
    background-color: grey;
    display: flex;
    flex-direction: row;
    align-items: space-around;
    justify-content: center;
  }
</style>
