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
                <b-col v-for="item in popularlist" :key="item.id" md="4" style="margin: 1em auto">
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
                price: 5000,
                place:"Traditional Apartments",
                type: "for sale",
                attribute:{
                    beds:3,
                    wc:2,
                    carpark: 2
                }
            },
            {
                id:2,
                price: 5000,
                place:"Traditional Apartments",
                type: "for sale",
                attribute:{
                    beds:3,
                    wc:2,
                    carpark: 2
                }
            },
            {
                id:3,
                price: 5000,
                place:"Traditional Apartments",
                type: "for sale",
                attribute:{
                    beds:3,
                    wc:2,
                    carpark: 2
                }
            },
             {
                id:4,
                price: 5000,
                place:"Traditional Apartments",
                type: "for sale",
                attribute:{
                    beds:3,
                    wc:2,
                    carpark: 2
                }
            },
             {
                id:5,
                price: 5000,
                place:"Traditional Apartments",
                type: "for sale",
                attribute:{
                    beds:3,
                    wc:2,
                    carpark: 2
                }
            },
             {
                id:6,
                price: 5000,
                place:"Traditional Apartments",
                type: "for sale",
                attribute:{
                    beds:3,
                    wc:2,
                    carpark: 2
                }
            },]
        }
    }
}
</script>
<style scoped>
    #popular{
        background-color: #d9d6d1;
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

</style>