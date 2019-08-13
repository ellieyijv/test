<template>
  <div>
    <topHeader />
    <topNavigation />
    <nuxt />
  </div>
</template>

<script>
import topHeader from "../components/share/topHeader"
import topNavigation from "../components/share/topNavigation"
export default {
    components:{topHeader, topNavigation}
}
</script>

<style scoped>

</style>
