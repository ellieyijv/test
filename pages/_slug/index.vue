<template>
<b-container>
    <b-row class="mt-3">
        <b-col cols="7">
            <b-row class="imgShow" :style="{ backgroundImage: `url(${backgroundUrl})` }">
                
            </b-row>
            <b-row class="pt-3" >
                <b-col cols="4" v-for="(image,index) in smallImages" :key="index">
                    <img style="width:200px; height:200px" :src="image.imageUrl" @click="showBigImage(image)"/>
                </b-col>
            </b-row>
 
        </b-col>
    </b-row>
</b-container>
</template>

<script>
export default {
    data(){
        return{
            backgroundUrl: '/banner_mobile.png',
            smallImages:[
                {
                    imageUrl: '/banner_mobile.png'
                },
                {
                    imageUrl: '/homepage/apartment.png'
                },
                  {
                    imageUrl: '/banner_mobile.png'
                }
            ]
        }
    },
    methods:{
        showBigImage(image){
            return this.backgroundUrl = image.imageUrl
        }
    }
}
</script>

<style scoped>
    .imgShow{
        background: url('/homepage/apartment.png') no-repeat ; 
        height:400px;
        background-size: cover;
    }
</style>