<template>
  <div class="container-fluid">
    <banner />
    <description />
    <popularListing />
    <discoverHome />
    <findPerfectPlace />
    <service />
    <meetAgence />
    <realestatePartners />
  </div>
</template>

<script>

import banner from "../components/HomePage/banner"
import description from "../components/HomePage/description"
import popularListing from "../components/HomePage/popularListing"
import discoverHome from "../components/HomePage/discoverHome"
import findPerfectPlace from "../components/HomePage/findPerfectPlace"
import service from "../components/HomePage/service"
import meetAgence from "../components/HomePage/meetAgence"
import realestatePartners from "../components/HomePage/realestatePartners"
export default {
  components: {
      banner, description, popularListing, discoverHome, findPerfectPlace, service, meetAgence, realestatePartners
  },
 
}
</script>

<style scoped>
  .container-fluid{
    padding:0;
  }
</style>
