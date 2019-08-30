<template>
  <div>
    <login/>
    <add-album/>
  </div>
</template>

<script>
  import Login from "./../components/admin/Login"
  import AddAlbum from "./../components/admin/AddAlbum"

  export default {
    name: "admin",
    components: {
      Login,
      AddAlbum
    },
    data() {
      return {
          
      }
    }
  };
</script>
