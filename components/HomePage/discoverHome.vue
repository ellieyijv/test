<template>
    <b-container fluid id="discover">
        <div class="title">
            <p>Discover A Home You'll Love To Stay</p>
        </div>
        <div id="map-wrap" style="height: 40vh">
            <no-ssr>
                <l-map :zoom='zoom' :center="center">
                    <l-tile-layer :url="url"></l-tile-layer>
                    <l-marker 
                            v-for="(item, index) in places"
                            :key="index"
                            ref="markersRef"
                            :lat-lng="[item.lattitude, item.longitude]"
                            @mouseover="mouseOver(index)"
                            @mouseleave="mouseLeave(index)"
                            :draggable="true"
                            
                    >
                        <l-icon :icon-size="iconSize"
                                :icon-url="item.icon">
                        </l-icon>
                        <l-popup >

                        </l-popup>
                    </l-marker>
                   
                </l-map>
            </no-ssr>
           
        </div>
    </b-container>
</template>

<script>

import productCard from "../share/productCard"
export default {
    components: {productCard},
   data(){
       return{
            zoom: 13,
            center: [47.413220, -1.219482],
            url: "https://tile.thunderforest.com/landscape/{z}/{x}/{y}.png?apikey=f04c14cffa4142c195223b4562189a95",
            places:[
               {
                    lattitude: 47.413220,
                    longitude: -1.219482,
                    icon: "/homepage/map-icon.png",
                    img : "/homepage/popularlist.png",
                    title: "modern house",
                    address: "33 avenue hornsby, NSW"
                },
                {
                    lattitude: 46.413220,
                    longitude: -1.219482,
                    img : "/homepage/popularlist.png",
                    icon: "/homepage/map-icon.png",
                    title: "modern apartment",
                    address: "33 avenue hornsby, NSW"
                },
                {
                    lattitude: 33.413220,
                    longitude: -1.219482,
                    img : "/homepage/popularlist.png",
                    icon: "/homepage/map-icon.png",
                    title: "modern house",
                    address: "33 avenue hornsby, NSW"
                }],
            iconSize: [20, 20],
            markerObjects: null
          
       }
   },
   
  

    methods: {
       mouseOver(index){
            let item = this.places[index];
            this.markerObjects = this.$refs.markersRef.map(ref => ref.mapObject); 
            let marker = this.markerObjects[index];
            item.icon = "/homepage/map-icon-click.png"  
            marker.bindPopup(`<div><img src=${item.img} style="width:100%;"/><h6>${item.title}</h6><p>${item.address}</p></div>`).openPopup();
       },
       mouseLeave(index){
          this.places[index].icon = "/homepage/map-icon.png"
       }
   },
   

}
</script>

<style scoped>
    #discover .title{
        background-color: #39524f;
        text-align: center;
    }
    #discover p{
        color:white;
        padding:1em;
        margin-bottom: 0;
    }


</style>