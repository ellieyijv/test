<template>
     <b-container fluid id="perfect-place">
        <div style="text-align:center"> 
            <p>Popular Cities</p>
            <h5>Find Perfect Place</h5>
            <b-container>
                <b-row>
                    <b-col v-for="item in perfectList" :key="item.id" md="4" cols="12" sm="6" style="margin: 1em auto">
                        <b-card :img-src="item.categoryImg" 
                                img-alt="Image" 
                                overlay 
                                text-variant="white"> 
                                <div class="card-content pt-xl-3">
                                    <b-card-title>{{item.category}}</b-card-title>
                                    <b-card-sub-title>{{item.quantity+ 'Listings'}}</b-card-sub-title>
                                </div>  
                        </b-card>
                    </b-col>
                </b-row>
            </b-container>
        </div>
    </b-container>
</template>

<script>
export default {
    data(){
        return{
            perfectList:[
                {
                    category: 'house',
                    categoryImg: '/homepage/house.png',
                    quantity: 5
                },
                {
                    category:'apartment',
                    categoryImg: '/homepage/apartment.png',
                    quantity: 10
                },
                {
                    category: 'studio',
                    categoryImg: '/homepage/studio.png',
                    quantity: 20
                }]
        }
    }
}
</script>

<style scoped>
    @media (max-width:576px){
        .card{
            width:70%;
            margin:auto;
        }
    }

    #perfect-place{
        margin:4rem auto;
    }

    #perfect-place p{
        color: #797979;
        font-size:14px;
        margin-bottom: 0;
    }

    #perfect-place h5{
        font-size:30px;
        font-weight: normal; 
        margin-bottom: 2rem;
    }
    .card-img-overlay{
        padding:0 !important;
        height:20%;
        background-image: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #000000 100%);
        position:absolute;
        bottom:0;
        top:auto;
    }
    
    .card-content {
        text-align: left;
        margin-left:1rem;
        
    }
    .card-title{
        font-size:18px;
       
    }
    .card-subtitle{
        font-size:14px;
        font-weight: normal;
    }

</style>