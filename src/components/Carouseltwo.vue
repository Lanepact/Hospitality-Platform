<template>
    <section id="carouseltwo">

<div class="carousel slide" data-ride="false" id="carouselslidetwo">
      <div class="carousel-inner">
        <div class="carousel-item active container-fluid ">
            <div class="row">
          <div class="col colone coloneimgone">

          </div>
          <div class="col coltwo">
              <h3 class="carousel-text">Sheraton Downtown Denver Hotel</h3>
          </div>
            </div>
        </div>
        <div class="carousel-item container-fluid" > 
          <div class="row">
          <div class="col colone coloneimgtwo">

          </div>
          <div class="col coltwo">
              <h3 class="carousel-text">Sheraton Grand Hotel Dubai</h3>
          </div>
            </div>
        </div>
        <div class="carousel-item container-fluid ">
           <div class="row">
          <div class="col colone coloneimgthree">

          </div>
          <div class="col coltwo">
              <h3 class="carousel-text">Sheraton Guanzhou Hotel</h3>
          </div>
            </div>
        </div>
      </div>
       <button class="carousel-control-prev" type="button" data-bs-target="#carouselslidetwo" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>

  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carouselslidetwo" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
  </button>
    </div>

</section>
</template>

<script>
export default {
    name:'Carouseltwo',
}
</script>
<style scoped>
#carouselslidetwo{
   
    padding-left: 0;
    padding-right: 0;
    background-color: whitesmoke;
    padding-right: 0;
    margin: 0;
}
.colone{
    
    width:70%;
    height: 500px;
    padding:50px;
    text-align: center;
}
.coltwo{
    background-color: white ;
    height: 300px;
    margin-left: 40px;
    margin-top: 10%;
    margin-right: 4%;
    margin-bottom: 0;
    padding:50px;
    text-align: center;
}
.coloneimgone{
  background: url('~@/assets/imgone.jpg') no-repeat center ;
}
.coloneimgtwo{
  background: url('~@/assets/imgtwo.jpg') no-repeat center ;
}
.coloneimgthree{
  background: url('~@/assets/imgthree.jpg') no-repeat center ;
}
.carousel-text{
  padding: 15%;
}

</style>