<template>
    <b-container fluid id="service">
        <b-container>
            <div class="service-title">
                <p>Best Standard</p>
                <h4>Service You Need</h4>
            </div>
            <b-row>
                <b-col  md="4" lg="4" sm="6" class="my-lg-5 my-sm-3 my-3 my-md-5 item" v-for="(item, index) in services" :key="index">
                    <div class="service-card p-3 p-sm-4 p-lg-5">
                        <img :src="item.icon" alt="servce"/>
                        <h5>{{item.title}}</h5>
                        <p>{{item.description}}</p>
                    </div>
                </b-col>    
            </b-row>
        </b-container>
    </b-container>
</template>

<script>
export default {
    data(){
        return{
            services: [
                {
                    icon: "/homepage/service1.png",
                    title: "Perfect Tools",
                    description: "Nam nec tellus a odio tincidunt a ornare odio. Mauris vitae erat consequat auctor eu in elit."
                },
                  {
                    icon: "/homepage/service2.png",
                    title: "Search in Clink",
                    description: "Nam nec tellus a odio tincidunt a ornare odio. Mauris vitae erat consequat auctor eu in elit."
                },
                  {
                    icon: "/homepage/service3.png",
                    title: "User Control",
                    description: "Nam nec tellus a odio tincidunt a ornare odio. Mauris vitae erat consequat auctor eu in elit."
                }]
        }
    }
}
</script>

<style scoped>
    #service{
        background-image: linear-gradient(rgba(57, 82, 79, 0.9), rgba(57, 82, 79, 0.9)), url("/homepage/service-background.png");
    }

    .service-title{
        color:white;
        text-align: center;
        padding-top: 3rem;
        
    }
    .service-title p{
        font-size: 14px;
        margin-bottom: 0;
    }
    .service-title h4{
        font-weight: normal;
        font-size: 30px;
        margin-bottom: 0;
    }
    .service-card{
        background-color: white;
        margin: auto auto;
        text-align: center;
    }
    .service-card img{
        margin-bottom: 2rem;
    }
    .service-card  h5{
        font-size: 18px;
        font-weight: normal;
    }
    .service-card p{
        font-size:13px;
        color: #494949;
    }
    @media (max-width:768px) {
        .item:last-child{
           margin-bottom: 3rem !important;
        }
    }

    @media (max-width: 576px){
        .service-card{
            width:60vw;
        }
    }
</style>