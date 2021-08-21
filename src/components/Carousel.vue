<template>
    <section id="carouselslide">

<div class="carousel slide" data-ride="false" id="carousel">
      <div class="carousel-inner">
        <div class="carousel-item active container-fluid itemone ">
            <div class="message">
          <h2>See the world</h2>
          <p>Find us at the heart of hundreda of communities around 70+ countries</p>
            </div>
        </div>
        <div class="carousel-item container-fluid itemtwo" > 
           <div class="message">
          <h2>See the world</h2>
          <p>Find us at the heart of hundreda of communities around 70+ countries</p>
            </div>
        </div>
        <div class="carousel-item container-fluid itemthree">
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
}
.itemtwo{
    background: url('~@/assets/imagetwo.jpg') no-repeat center ;
}
.itemthree{
    background: url('~@/assets/imagethree.jpg') no-repeat center ;
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
</style>