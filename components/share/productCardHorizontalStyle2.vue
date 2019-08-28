<template>
    <div>
        <b-card no-body class="overflow-hidden"  style="max-width:540px;" id="productCardHorizontalStyle2">
            <b-row no-gutters>
                <b-col sm="4">
                    <b-card-img src="/homepage/popularlist.png" class="rounded-0"></b-card-img>
                </b-col>
                <b-col sm="8">
                    <b-card-body>
                        <b-card-title class="mt-sm-n3 mb-sm-3">{{item.propertyName}}</b-card-title>
                        <b-card-sub-title class="mb-sm-1">${{item.price}}</b-card-sub-title>
                        <b-car-text>{{item.address}}</b-car-text>       
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
    #productCardHorizontalStyle2{
        border: none;
        border-radius:0;
    }
    #productCardHorizontalStyle2 .card-title{
        font-size: 14px;
     
    }
    #productCardHorizontalStyle2 .card-subtitle{
        color: #F3755E !important;
    }
    #productCardHorizontalStyle2 b-car-text{
        font-size:13px;
        color: #6c757d;
    }
    
</style>