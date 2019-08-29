<template>
    <div>
        <b-card no-body class="overflow-hidden" style="max-width: 750px;" id="productCardHorizontal">
            <b-row no-gutters>
                <b-col md="4" sm="5" style="position:relative">
                    <b-card-img src="/homepage/popularlist.png" class="rounded-0"></b-card-img>
                    <div class="price" >
                        <span class="pl-2">${{item.price}}</span>
                        <b-button class="btn  pull-right" type="button" >{{item.attributes.listType}}</b-button>
                    </div>
                </b-col>
                <b-col md="8" sm="7">
                    <b-card-body style="height:100%;">
                        <div style="height:65%">
                            <b-card-title>{{item.propertyName}}</b-card-title>
                            <b-card-sub-title>{{item.address}}</b-card-sub-title>
                            <b-card-text class="property-attributes py-3">
                                <span >{{item.description.bedrooms}}bedrooms</span>
                                <span class="px-1">{{item.description.bathrooms}} baths</span>
                                <span class="px-1">area:{{item.description.landSize}}sqm</span>
                            </b-card-text>
                        </div>
                        <b-card-text  style="border-top: solid 1px rgba(0,0,0,0.125); height:35%;" class="card-bottom py-1">
                          <div class="py-4 py-sm-2">
                            <span>25 days ago</span>
                            <button class="btn btn-outline-danger pull-right" type="button" id="toright">View More</button>
                          </div>
                        </b-card-text>  
                    </b-card-body>
                    
                </b-col>
            </b-row>
        </b-card>
    </div>
</template>

<script>
export default {
    props: ['item']
}
</script>

<style scoped>
    #productCardHorizontal .card-title{
        font-size: 18px;
    }
    #productCardHorizontal .card-subtitle,  #productCardHorizontal .property-attributes{
        font-size: 13px;
    }

    #productCardHorizontal .card-bottom{
        font-size: 13px;
        color:#949494;
        vertical-align: middle;
    }
    #productCardHorizontal .price{
        position:absolute;
        bottom:0;
        width:100%;
        font-size:18px;
        font-weight:bold;
        color:white;
        background-image: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #000000 100%);
    }
    #productCardHorizontal .price button{
        margin-right:1rem;
        margin-bottom:0.5rem;
        font-size:12px;
        font-weight:bold;
    }

    
</style>