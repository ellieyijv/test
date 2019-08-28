<template>
    <b-container id="top-footer">
        <b-row align-v="start">
            <b-col sm="6" md="4" cols="12">
                <img src="/footer-logo.png" />
            </b-col>
            <b-col cols="3"  offset-sm="0" offset="1" sm="2" class="p-1">
                <h5>Site</h5>
                    <ul>
                        <li>Buy</li>
                        <li>Sell</li>
                        <li>Rent</li>
                        <li>Service</li>
                    </ul>
            </b-col>
            <b-col cols="5" sm="3" md="2" class="p-1">
                <div>
                <h5>Helpful Links</h5>
                    <ul>
                        <li>Half Map</li>
                        <li>Register</li>
                        <li>Pricing</li>
                        <li>Add Listing</li>
                    </ul>
                </div>
            </b-col>
            <b-col cols="10" sm="10" md="4"  offset="1" offset-sm="1" offset-md="0" class="p-1">
                 <div><h5>About</h5>
                     <p>Nam nec tellus a odio tincidunt auctor a ornare odio. Sed non mauris vitae erat consequat auctor eu in elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos.</p>
                 </div>
            </b-col>
        </b-row>
    </b-container>
</template>

<style scoped>
    #top-footer{
        margin:4rem auto;
        color:#494949;
    }
    #top-footer li, #top-footer p{
        list-style: none;
        font-size:13px; 
    }
    #top-footer h5{
        font-size:14px;
    }

    #top-footer ul, #top-footer p{
        padding-left:0;
        padding-top:0.5rem;
    }
</style>