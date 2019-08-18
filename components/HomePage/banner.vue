<template>
    <b-container fluid  class="banner">
      <b-container class="content"> 
            <h3 class="title">Discover the best property in one place</h3>
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
   } 
}
</script>
<style scoped>
    .banner{
        display:flex;
        height: 60vh;
        background: url("/banner_image.png")  ; 
    }
    .content{
        margin: auto auto;
        text-align: center; 
        width:70%;
    }
    .content h3{
         font-size:36px;
         color:#fff;
         margin-bottom:1em;
    }

    @media (max-width: 768px){
        .content h3{
            font-size:24px;
        }
    }
   
</style>