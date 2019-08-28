<template>
    <b-container fluid id="discover">
        <div class="title">
            <p>Discover A Home You'll Love To Stay</p>
        </div>
        <mapComponent style="height: 40vh; width:100vw;"/>
    </b-container>
</template>

<script>

import mapComponent from "../share/mapComponent"

export default {
    components: {mapComponent},
 

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