<template>
    <b-container fluid id="buy">
        <mapComponent style="height: 48vh; width:100vw;"/>
        <b-container class="buy-list">
            <b-row>
                <b-col cols="12" sm="12" md="8" >
                    <b-dropdown size="sm" split split-variant="outline-none" variant="none" toggle-class="text-decoration-none" no-caret>
                        <template slot="button-content"><span style="color:#494949; padding-left:10px;">Sort by:</span>Relevant</template>
                        <b-dropdown-item href="#">Action</b-dropdown-item>
                        <b-dropdown-item href="#">Another action</b-dropdown-item>
                        <b-dropdown-item href="#">Something else here...</b-dropdown-item>
                    </b-dropdown>
            
                    <span v-for="(item, index) in saleItems" :key="index" >
                        <productCardHorizontal :item="item" class="mb-4"/>
                    </span>
                </b-col>
                <b-col cols="12" sm="12" md="4" class="mt-2 pl-5">
                    <fiterComponent />

                    <h6 style="color:black;" class="mt-4 mb-3">FEATURED PROPERTY</h6>
                    <productCard :item="saleItems[0]" />

                    <h6 style="color:black;" class="mt-4 mb-3">CATEGORIES</h6>
                    <div v-for="category in categories" :key="category.name" class="buy-category">
                        <b-row>
                            <b-col cols="auto" class="mr-auto"><span class="pr-3">></span><span style="color: #F3755E">{{category.name}}</span></b-col>
                            <b-col cols="auto">{{category.quantity}}</b-col>
                        </b-row>
                    </div>

                    <h6 style="color:black;" class="mt-4 mb-3">POPULAR LISTING</h6>
                     <span v-for="(item, index) in saleItems.slice(1,4)" :key="index" >
                        <productCardHorizontalStyle :item="item"/>
                    </span>
                </b-col>
            </b-row>
        </b-container>
    </b-container>
</template>

<script>
import mapComponent from "../components/share/mapComponent"
import productCardHorizontal from "../components/share/productCardHorizontal"
import fiterComponent from "../components/share/filterComponent"
import productCard from "../components/share/productCard"
import productCardHorizontalStyle from "../components/share/productCardHorizontalStyle2"
export default {
    components:{
        mapComponent, productCardHorizontal, fiterComponent, productCard, productCardHorizontalStyle
    },
    data(){
        return{
           
            categories:[{
                name: "House",
                quantity: 17
            },
            {
                name: "Townhouse",
                quantity: 15
            },
            {
                name: "Villa",
                quantity: 17
            },
            {
                name: "Apartment",
                quantity: 6
            }],
            saleItems:[{
                price: 555,
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
                price: 555,
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
                price: 555,
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
                price: 555,
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
                price: 555,
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
                price: 555,
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
            }]
        }
    }
}
</script>

<style scoped>
   #buy{
       padding:0;
   }

   #buy .buy-list{
       margin: 4rem auto;
   }

   #buy .b-dropdown{
       margin-bottom:1rem;
   }
   #buy .buy-category{
        font-size:14px; 
        color:  #6c757d;
    }

 
</style>