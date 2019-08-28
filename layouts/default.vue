<template>
    <section>
        <div v-if="$device.isMobile"> 
            <topNavigation />
            <nuxt />
            <bottomFooter />
        </div>
        <div v-else>
            <topHeader/>
            <topNavigation />
            <nuxt />
            <bottomFooter />
        </div>
    </section>
</template>

<script>
import topHeader from "../components/share/topHeader"
import topNavigation from "../components/share/topNavigation"
import bottomFooter from "../components/share/bottomFooter"
export default {
    components:{topHeader, topNavigation, bottomFooter}
}
</script>

<style>
    .btn-style{
        color: #f3755e;
        border-color:#f3755e;
        border-radius:30px;
        padding: 0.3em 1.5em;
        font-size: 14px;
    }
    .btn-style .active{
        color: white;
        background-color: #f3755e;
    }
    body{
        font-family: 'Poppins', sans-serif;
    }
</style>
