<template>
  <div class="container-fluid">
    <banner />
    <description />
    <popularListing />
    <discoverHome />
   
  </div>
</template>

<script>

import banner from "../components/HomePage/banner"
import description from "../components/HomePage/description"
import popularListing from "../components/HomePage/popularListing"
import discoverHome from "../components/HomePage/discoverHome"

export default {
  components: {
    banner, description, popularListing, discoverHome
  }
}
</script>

<style scoped>
  .container-fluid{
    padding:0;
  }
</style>
