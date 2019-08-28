<template>

    <b-form id="filter-form" >
        <h6 style="color:black;" class="mb-3">PROPERTY SEARCH</h6>
        <b-form-group id="input-group-address">
            <b-form-input
            id="input-address"
            v-model="form.address"
            required
            placeholder="Enter Address, City or State"
            ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-type">
            <select
                id="input-type"
                v-model="form.type"
                class="selectpicker" 
                multiple
                title="Any Type"
            >
            <option>House</option>
            <option>Apartment&Unit</option>
            <option>TownHose</option>
            </select>
            
        </b-form-group>
 
        <b-form-group id="input-group-minPrice">
            <b-form-input
            id="input-minPrice"
            v-model="form.minPrice"
            placeholder="Min Price"
            ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-max-price">
            <b-form-input
            id="input-max-price"
            v-model="form.maxPrice"
            placeholder="Max Price"
            ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-bedrooms">
            <b-form-input
            id="input-bedrooms"
            v-model="form.bedrooms"
            placeholder="Bedrooms"
            ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-features" class="py-2">
            <h6>More Features</h6>
            <b-form-checkbox-group v-model="form.checked" id="checkboxes-features" class="row">
                
                <div v-for="(item, index) in features" :key="index" class="col-6" >   
                    <b-form-checkbox :value="item" >{{item}}</b-form-checkbox>
                </div>
            </b-form-checkbox-group>
        </b-form-group>
        <b-button type="submit" variant="danger" block class="search-btn py-2">Search</b-button>
    </b-form>
    
</template>

<script>
export default {
    data(){
        return{
            form: {
                address: '',
                type:[],
                minPrice: '',
                maxPrice: '',
                bedrooms: '',
                checked: []
            },
            types:[ 'House', 'TownHose', 'Villa', 'Apartment&Unit'],
            features:['Parking', 'Gym', 'Air Conditioner', 'Wireless Internet', 'Washing Machine', 'Elevator', 'Heating', 'Swimming pool']
        }
    }
}
</script>

<style>
    #filter-form{
        color: #6c757d;
        font-size: 13px;
    }

    .bootstrap-select{
        width:100% !important;
        background-color: white;
    }

    #input-group-type{
        border: 1px solid #ced4da;
    }

    #input-group-type .btn-light{
        background-color: white !important;
        color: #6c757d;
    }

    #filter-form .search-btn{
        background: #F3755E;
        border-radius: 50px;
        border:none;
        font-size:14px;
    }
</style>