<template>
    <b-container fluid  class="banner" id="hero-banner" :style="{background: 'url(' + imgUrl + ')'}">
      <b-container class="content"> 
            <h3 class="title">Discover The Best Property In One Place</h3>
            <span v-if="$device.isMobile">
            </span>
            <span v-else>
                <search />
            </span>      
      </b-container>
    </b-container>
</template>

<script>
import search from "../share/search"
export default {
   components: {
       search
   },
   data(){
       return{
           imgUrl: this.$device.isMobile? '/banner_mobile.png': '/banner_image.png'
       }
   }
}
</script>
<style scoped>
    #hero-banner{
        display:flex;
        height:60vh ;
    }
    #hero-banner .content{
        margin: auto auto;
        text-align: center; 
        width:90%;
    }
    #hero-banner .content h3{
         font-size:36px;
         color:#fff;
         margin-bottom:1em;
         font-weight:bold;
    }

    @media (max-width: 768px){
        #hero-banner .content h3{
            font-size:24px;
        }
        #hero-banner {
            height:45vh;
        }
    }
   
</style>