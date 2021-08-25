<template>
    <section id="carouselslide">

<div class="carousel slide" data-ride="false" id="carousel">
      <div class="carousel-inner">
        <div class="carousel-item active container-fluid itemone img">
            <div class="message">
          <h2>See the world</h2>
          <p>Find us at the heart of hundreda of communities around 70+ countries</p>
            </div>
        </div>
        <div class="carousel-item container-fluid itemtwo img" > 
           <div class="message">
          <h2>See the world</h2>
          <p>Find us at the heart of hundreda of communities around 70+ countries</p>
            </div>
        </div>
        <div class="carousel-item container-fluid itemthree img">
           <div class="message">
          <h2>See the world</h2>
          <p>Find us at the heart of hundreda of communities around 70+ countries</p>
            </div>
        </div>
      </div>
       <button class="carousel-control-prev" type="button" data-bs-target="#carousel" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>

  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carousel" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
  </button>
    </div>

</section>
</template>

<script>
export default{
    name:'Carousel',
}
</script>

<style scoped>
.itemone{
    background: url('~@/assets/imageone.jpg') no-repeat center ;
    background-size: cover;
}
.itemtwo{
    background: url('~@/assets/imagetwo.jpg') no-repeat center ;
     background-size: cover;
}
.itemthree{
    background: url('~@/assets/imagethree.jpg') no-repeat center ;
     background-size: cover;
}
.message{
    text-align: center;
    background-color:rgba(245, 245, 245, 0.685);
    width:30%;
    margin-left: 0;
    margin-top: 10%;
    margin-bottom: 30%;
    padding: 15px;
}

@media (max-width: 500px){
  .message{
    width: 50%;
  }
  #carouselslide{
    padding-top:10px ;
  }
  .img{
    background-size: cover;
  }
}
/* tablet */
@media (max-width: 800px){
  .message{
    width: 50%;
  }
  #carouselslide{
    padding-top:10px ;
  }
  .img{
    background-size: cover;
  }
}
</style>