<template>
    <b-container fluid id="popular">
        <div style="text-align:center"> 
            <p>Discover</p>
            <h5>Popular Listing</h5>
            <div>
                <button class="btn btn-outline-danger active">All</button>
                <button class="btn btn-outline-danger">FOR SALE</button>
                <button class="btn btn-outline-danger">FOR RENT</button>
            </div>
            <b-container>
            <b-row>
                <b-col v-for="item in popularlist" :key="item.id" md="4" sm="6" cols="12" style="margin: 1em auto">
                    <productCard :item = "item"/>
                </b-col>
            </b-row>
            <b-row>
                <button class="btn btn-outline-danger active" style="margin:1em auto" >More Listings</button>
            </b-row>
            </b-container>
        </div>
    </b-container>
</template>

<script>
import productCard from "../share/productCard"
export default {
    components: {productCard},
    data(){
        return{
            popularlist: [{
                id:1,
                price: '550,000',
                attributes:{
                    listType: 'FOR SALE'
                },
                propertyName: 'Traditional Apartments',
                description:{
                    bedrooms:3,
                    bathrooms: 2,
                    parkings: 1,
                    landSize: 240
                },
                address:'33 girdsaf hornsby'
                
            },
            {
                id:2,
                price: '550,000',
                attributes:{
                    listType: 'FOR SALE'
                },
                propertyName: 'Traditional Apartments',
                description:{
                    bedrooms:3,
                    bathrooms: 2,
                    parkings: 1,
                    landSize: 240
                },
                address:'33 girdsaf hornsby'
                
            },
            {
                id:3,
                    price: '550,000',
                attributes:{
                    listType: 'FOR SALE'
                },
                propertyName: 'Traditional Apartments',
                description:{
                    bedrooms:3,
                    bathrooms: 2,
                    parkings: 1,
                    landSize: 240
                },
                address:'33 girdsaf hornsby'
            },
             {
                id:4,
                    price: '550,000',
                attributes:{
                    listType: 'For Sale'
                },
                propertyName: 'Traditional Apartments',
                description:{
                    bedrooms:3,
                    bathrooms: 2,
                    parkings: 1,
                    landSize: 240
                },
                address:'33 girdsaf hornsby'
            },
             {
                id:5,
                     price: '550,000',
                attributes:{
                    listType: 'For Sale'
                },
                propertyName: 'Traditional Apartments',
                description:{
                    bedrooms:3,
                    bathrooms: 2,
                    parkings: 1,
                    landSize: 240
                },
                address:'33 girdsaf hornsby'
            },
             {
                id:6,
                     price: '550,000',
                attributes:{
                    listType: 'For Sale'
                },
                propertyName: 'Traditional Apartments',
                description:{
                    bedrooms:3,
                    bathrooms: 2,
                    parkings: 1,
                    landSize: 240
                },
                address:'33 girdsaf hornsby'
            },]
        }
    }
}
</script>
<style scoped>
    #popular{
        background-color: rgba(217, 214, 209, 0.4);
        padding: 4em 0;
    }
    #popular .btn-outline-danger{
        margin:2em 1em;
        color: #f3755e;
        border-color:#f3755e;
        border-radius:30px;
        padding: 0.3em 1.5em;
        font-size: 14px;
    }
    #popular .btn-outline-danger:hover, #popular .btn-outline-danger.active{
        color: white;
        background-color: #f3755e;
    }
    #popular p{
        color: #797979;
        font-size:14px;
        margin-bottom: 0;
    }

    #popular h5{
        font-size:30px;
        font-weight: normal; 
    }

    @media (max-width:499px) {
        #popular .btn-area button{
            margin: 2em 0.5em;
        }
    }
    @media (max-width:576px) {
         #popular .card{
           width:80vw;
           margin:auto;
        }
    }

</style>