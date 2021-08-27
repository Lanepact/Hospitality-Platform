<template>
    <section id="card">
        <div class="container web-view">
  <div class="row ">
    <div class="col colone">
      <h1>DISCOVER YOUR WORLD</h1>
      <p>Marriott Bonvoy™ gives you access to world-class benefits, free nights, exclusive experiences and so much more.</p>
      <span> <a href="/signin">SIGN IN</a> <a href="/signup">JOIN NOW</a> </span>
    </div>
    <div class="col coltwo ">
      
  </div>
</div>
    </div>


<div class="container mobile-view">
  <div class="row ">
    <div class="col coltwo ">
      
  </div>

   <div class="col colone ">
      <h1>DISCOVER YOUR WORLD</h1>
      <p>Marriott Bonvoy™ gives you access to world-class benefits, free nights, exclusive experiences and so much more.</p>
      <span> <a href="/signin">SIGN IN</a> <a href="/signup">JOIN NOW</a> </span>
    </div>
</div>
    </div>

    </section>
</template>

<script>

export default {
    name:'Card',
}
</script>

<style scoped>
.container{
    width: 70%;
    background-color: whitesmoke;
    margin-bottom: 5%;
}

.coltwo{
     background: url('~@/assets/card.jpg') no-repeat center ;
    height: 300px;
    margin-left: 40px;
    margin-right: 4%;
    margin-bottom: 0;
    padding:50px;
    text-align: center;
}
.mobile-view{
  display: none;
}
/* mobile */
@media (max-width: 500px){
  #card{
    background-color: whitesmoke;
}
.web-view{
  display: none;
}
 .mobile-view{
   display: inline;
 }
 .container{
   width: 100%;
   
 }
 .coltwo{
   width: 100%;
 }
 .colone{
   width: 100%;
   margin-left: 0;
  
 }

}

/* tablet */
@media (max-width: 800px){
  #card{
    background-color: whitesmoke;
}
.web-view{
  display: none;
}
 .mobile-view{
   display: inline;
 }
 .container{
   width: 100%;
   
 }
 .coltwo{
   padding: 25%;
   width: 100%;
   
 }
 .colone{
   padding: 10%;
   width: 100%;
   text-align: left;
   margin-left: 0px;
 }
}
</style>