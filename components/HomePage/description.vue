<template>
    <b-container id="description">
        <b-row>
        <b-col md="6" style="margin:auto; padding:0 2em">
            <h5>Homes around the world</h5>
            <p class="pt-3">Nam nec tellus a odio tincidunt auctor a ornare odio. Sed non mauris vitae erat consequat auctor eu in elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos.</p>
            <button class="btn btn-outline-danger mt-3">View More</button>
        </b-col>
        <b-col md="6">
            <div class="image-part">
            </div>
        </b-col>
        </b-row>
    </b-container>
</template>

<style scoped>
    #description{
        margin: 2em auto;
    }

    #description h5{
        font-size:30px;
        font-weight:normal;
    }

    #description p{
        font-size:16px;
    }

    #description .btn-outline-danger{
        color: #f3755e;
        border-color:#f3755e;
        border-radius:30px;
        padding:0.5em 2em;
    }

    #description .btn-outline-danger:hover{
        color: white;
        background-color: #f3755e;
    }

    #description .image-part{
        background: url('/homepage/aroundworld.png') no-repeat;
        background-position: center center;
        background-size: cover;
        margin:3em 1em;
        height:24em;
        width:auto;
    }

    @media (max-width: 992px) {
        #description .image-part{
            height: 18em;
        }
         #description h5{
        font-size:20px;
        font-weight:normal;
    }

        #description p{
            font-size:13px;
        }
    }
</style>