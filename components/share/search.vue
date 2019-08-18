<template>
    <div class="container">
        <ul class="nav nav-tabs ml-4" id="search_component">
            <li class="nav-item">
                <a class="nav-link active" href="#">Buy</a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="#">Rent</a>
            </li>
        </ul>
        <b-form>
            <b-form-row>
                <b-col cols="6">hello</b-col>
                <b-col cols="2">dd</b-col>
                <b-col cols="4">dd</b-col>
            </b-form-row>
            <b-form-row>
                <b-col cols="3">hello</b-col>
                <b-col cols="3">dd</b-col>
                <b-col cols="2">dd</b-col>
                <b-col cols="4">dd</b-col>
            </b-form-row>
        </b-form>

    </div>
</template>


<script>
export default {
    
}
</script>

<style scoped>
 .nav-tabs .nav-link.active{
    background-color: #39524f !important;
    color: #fff;
    border:none;
    border-radius: 10px 10px 0 0;
    padding-left: 2em;  
    padding-right: 2em;
}

.nav-tabs .nav-link{
    background-color: #d9d6d1;
    color:#505050;
    border-radius: 10px 10px 0 0;
    padding-left: 2em;  
    padding-right: 2em;
    border:none;
}

form{
   background-color: white;
}

.form-row div{
    padding: 1em;
}


</style>