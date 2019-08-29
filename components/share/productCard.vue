<template>
        <b-card no-body class="overflow-hidden text-left" style="max-width: 750px;" id="productCard"  >
            <b-row no-gutters>
                <b-col cols="12" style="position:relative">
                    <b-card-img src="/homepage/popularlist.png" class="rounded-0"></b-card-img>
                    <div class="price  pl-1">
                        <span style="font-weight:bold">${{item.price}}</span>
                        <b-button class="btn  pull-right" type="button" >{{item.attributes.listType}}</b-button>
                    </div>
                </b-col>
                <b-col cols="12">
                    <b-card-body style="height:100%;" class="p-sm-1 p-md-3 pb-sm-0">
                        <span style="height:55%;" >
                            <b-card-title>{{item.propertyName}}</b-card-title>
                            <b-card-sub-title>{{item.address}}</b-card-sub-title>   
                            <b-row style="border-bottom: 1px #d9d6d1 solid; font-size:14px; color:#565656;" class="py-3 py-sm-3 ml-1">
                                <span class="pr-4"><img src="/homepage/bedsroom.png">{{item.description.bedrooms}}</span>
                                <span class="pr-4"><img src="/homepage/bath.png">{{item.description.bathrooms}}</span>
                                <span class="pr-4"><img src="/homepage/carparking.png">{{item.description.parkings}}</span>
                                <span class="pr-4"><img src="/homepage/lands.png">{{item.description.landSize}}​m<sup>2</sup></span>
                            </b-row>  
                            <b-row class="ml-1 pt-3 mr-1" style="color:#bcbcbc; ">
                                <span ><i class="fa fa-star-o" aria-hidden="true"></i></span>
                                <div class="ml-auto" style="font-size:13px"><img src="/homepage/calender.png">25 days ago</div>
                            </b-row>
                        </span>    
                    </b-card-body>              
                </b-col>
            </b-row>
        </b-card>
</template>

<script>
export default {
  props: ['item']
}
</script>

<style scoped>
    #productCard .card-title{
        font-size: 18px;
    }
    #productCard .card-subtitle{
        font-size: 13px;
    }
   
    #productCard .price{
        position:absolute;
        bottom:0;
        width:100%;
        font-size:18px;
        color:white;
        background-image: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #000000 100%);
    }
    #productCard  .price button{
        margin-right:1rem;
        margin-bottom:0.5rem;
        font-size:12px;
        font-weight:bold;
        background-color:#f3755e;
        border:none;
        border-radius:30px;
    }

   
</style>