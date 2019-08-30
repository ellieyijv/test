<template>
    <div class="container" id="search_component">
        <ul class="nav nav-tabs ml-4 mt-0 mt-sm-3 mt-md-0" >
            <li class="nav-item">
                <a class="nav-link active" href="#">Buy</a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="#">Rent</a>
            </li>
        </ul>
        <b-form class="search-form p-3">
            <b-form-row style="border-bottom: 1px solid #d9d6d1;" class="pb-3">
                <b-col sm="6" class="border-rightStyle pb-2 pb-md-0" >
                    <div style="text-align:left;" class="pt-1">
                        <span class="input-group-addon"><img src="/homepage/place-marker.png"></span>
                        <input style="width:90%; font-size:14px; height:39px" placeholder="Enter State, City or Postcode" />
                    </div>
                </b-col>
                <b-col sm="6" md="6" lg="2" class="border-rightStyle pb-2 pb-md-2 py-lg-0">
                    <select
                        class="selectpicker form-control" 
                        multiple
                        title="Property Type">
                        <option>House</option>
                        <option>Apartment&Unit</option>
                        <option>TownHose</option>
                    </select>
                </b-col>
                <b-col  md="12" lg="4" class="px-3">
                    <b-row style="font-size:14px; color:#565656;">
                        <b-col class="text-left">Price Range</b-col>  
                        <b-col class="text-right">${{value[0]}}-${{ value[1] }}</b-col>
                    </b-row>
                    <vue-slider :enableCross="false" :min="0" :max="1000000" :interval="5000" v-model="value"></vue-slider>
                </b-col>
            </b-form-row>
            <b-form-row class="pt-3">
                <b-col cols="6" md="3" class="border-rightStyle"> 
                    <select
                        class="selectpicker form-control" 
                        title="Min Bedrooms">
                        <option>1</option>
                        <option>2</option>
                        <option>3</option>
                    </select>
                </b-col>
                <b-col cols="6"  md="3" lg="2" class="border-rightStyle">
                    <select
                        class="selectpicker form-control" 
                        title="Min Bathrooms">
                        <option>1</option>
                        <option>2</option>
                        <option>3</option>
                    </select>
                </b-col>
                <b-col cols="6"  md="3" lg="2" class="border-rightStyle">
                    <select
                        class="selectpicker form-control" 
                        title="Min Parking">
                        <option>1</option>
                        <option>2</option>
                        <option>3</option>
                    </select>
                </b-col>
                <b-col cols="6" md="3" lg="2" class="border-rightStyle">
                    <select
                        class="selectpicker form-control" 
                        title="Min Area">
                        <option>1</option>
                        <option>2</option>
                        <option>3</option>
                    </select>
                </b-col>
                <b-col md="12" lg="2" class="pt-md-3 pt-lg-0 mx-auto pt-2">
                     <b-btn size="sm px-4 py-2" class="search-btn">
                         <i class="fa fa-search fa-rotate-90" aria-hidden="true"></i>
                            Search
                    </b-btn>
                </b-col>
            </b-form-row>
        </b-form>

    </div>
</template>


<script>
import VueSlider from 'vue-slider-component/dist-css/vue-slider-component.umd.min.js'
import 'vue-slider-component/dist-css/vue-slider-component.css'

// import theme
import 'vue-slider-component/theme/default.css'
export default {
    components: {VueSlider},
    data(){
        return{
            value: [0, 1000000],
        
        }
    },
    
}
</script>

<style>
    #search_component .border-rightStyle{
        border-right:1px #d9d6d1 solid;
    }
    #search_component .btn-light{
            background-color: white !important;
            border: none !important;
            font-size: 14px;
            color:#565656;
    }
    #search_component .nav-link.active{
        background-color: #39524f !important;
        color: #fff;
        border:none;
        border-radius: 10px 10px 0 0;
        padding-left: 2em;  
        padding-right: 2em;
    }

    #search_component .nav-tabs{
        border-bottom:none;
    }

    #search_component .nav-link{
        background-color: #d9d6d1;
        color:#505050;
        border-radius: 10px 10px 0 0;
        padding-left: 2em;  
        padding-right: 2em;
        border:none;
    }

    #search_component .search-form{
        background-color: white;
        border-radius:10px;
    }


    #search_component input{
        border:none;
        font-size:14px;
    }
    #search_component ::placeholder { /* Firefox, Chrome, Opera */ 
        color: #565656;
    } 
  
    #search_component  :-ms-input-placeholder { /* Internet Explorer 10-11 */ 
            color: #565656;
        } 
        
    #search_component  ::-ms-input-placeholder { /* Microsoft Edge */ 
            color: #565656; 
        } 
    #search_component .search-btn{
        color: white;
        background-color: #f3755e;
        border:none;
        border-radius:30px;       
    }

    #search_component .vue-slider-process{
        background-color:#f3755e !important
    }

</style>