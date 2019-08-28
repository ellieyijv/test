<template>
        <b-card no-body class="overflow-hidden text-left" style="max-width: 750px;" id="productCard">
            <b-row no-gutters>
                <b-col cols="12" style="position:relative">
                    <b-card-img src="/homepage/popularlist.png" class="rounded-0"></b-card-img>
                    <div class="price  pl-1">
                        <span>${{item.price}}</span>
                        <b-button class="btn  pull-right" type="button" >{{item.attributes.listType}}</b-button>
                    </div>
                </b-col>
                <b-col cols="12">
                    <b-card-body style="height:100%;">
                        <div style="height:55%">
                            <b-card-title>{{item.propertyName}}</b-card-title>
                            <b-card-sub-title>{{item.address}}</b-card-sub-title>     
                        </div>    
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