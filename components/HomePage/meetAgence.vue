<template>
     <b-container id="agences">
            <div class="agences-title">
                <p>Perfect Team</p>
                <h4>Meet Our Agents</h4>
            </div>
            <b-row>
                <b-col md="4" lg="3" sm="6" v-for="(item, index) in agences" :key="index">
                    <b-card :title="item.name" :img-src="item.thumbnail" img-alt="Image" img-top>
                        <b-card-text style="font-size:13px; color:#ACACAC">
                            {{item.position}}
                        </b-card-text>
                        <div slot="footer"><small style="color:#f3755e">
                             <i class="fa fa-phone p-2" aria-hidden="true"></i>{{item.phone}}
                            </small></div>
                        </b-card>
                </b-col>    
            </b-row>
        </b-container>
</template>

<script>
export default {
    data(){
        return{
            agences:[
                {
                    thumbnail:"/homepage/agence1.png",
                    name:"Tomas Chueng",
                    position:"A.Gent&Co Manager",
                    phone:"1-800-231-544"
                },
                  {
                    thumbnail:"/homepage/agence2.png",
                    name:"Tomas Chueng",
                    position:"A.Gent&Co Manager",
                    phone:"1-800-231-544"
                },
                  {
                    thumbnail:"/homepage/agence1.png",
                    name:"Tomas Chueng",
                    position:"A.Gent&Co Manager",
                    phone:"1-800-231-544"
                },
                  {
                    thumbnail:"/homepage/agence2.png",
                    name:"Tomas Chueng",
                    position:"A.Gent&Co Manager",
                    phone:"1-800-231-544"
                }]
        }
    }
}
</script>

<style scoped>
    #agences{
        margin:4rem auto;
        
    }
    .agences-title{
        padding-bottom:3rem;
        text-align: center
    }
    .agences-title p{
        font-size: 14px;
        margin-bottom: 0;
        color: #797979;
    }
    .agences-title h4{
        font-weight: normal;
        font-size: 30px;
        margin-bottom:0;
    }
    #agences .card{
        margin: 1rem auto;
    }

    #agences .card-title{
        font-size:18px;
    }
    @media (max-width:576px) {
         #agences .card{
           width:60vw;
        }
    }
</style>