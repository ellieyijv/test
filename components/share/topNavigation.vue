<template>
  <div class="container-fluid" id="top-nav">
    <b-container>
      <nav class="navbar navbar-expand-lg navbar-dark">
          <a class="navbar-brand" href="#">
              <img src="/agncologo.png" alt="logo" />
          </a>
          <button class="navbar-toggler" type="button" style="border:none" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon">
                <!-- <i class="fa fa-navicon"></i> -->
              </span>
          </button>
          <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
              <div class="navbar-nav">
                  <a class="nav-item nav-link active" href="#">Buy</a>
                  <a class="nav-item nav-link" href="#">Sell</a>
                  <a class="nav-item nav-link" href="#">Rent</a>
                  <a class="nav-item nav-link" href="#">About</a>
                  <a class="nav-item nav-link" href="#">Off the plan</a>
                  <a class="nav-item nav-link" href="#">contact</a>
              </div>
          </div>
      </nav>
    </b-container>
  </div>
</template>

<script>


export default {
  components: {
   
  }
}
</script>

<style scoped>
  #top-nav{
    background-color: #39524f;
  }

  #top-nav .nav-item{
    color:white; 
  }
  
  #top-nav .nav-item:hover, #top-nav .nav-item.active{
    color: #D9D6D1;
  }

 @media (min-width: 996px){
     #top-nav .nav-item{
       padding:1.5em;
     }
    }

  /* .fa.fa-navicon{
    color:white;
  } */

</style>
