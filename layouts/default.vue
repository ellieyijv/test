<template>
    <section>
        <div v-if="$device.isMobile"> 
            <topNavigation />
            <nuxt />
        </div>
        <div v-else>
            <topHeader />
            <topNavigation />
            <nuxt />
        </div>
    </section>
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
