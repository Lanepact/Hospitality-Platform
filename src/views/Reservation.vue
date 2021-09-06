<template>
    <section id="reservation">
    <div class="container webview">
      <h1>Superior King Room, Guest room, 1 King, City view, Corner room, Mid floor, Balcony</h1>
        <div class="row">
            <div class="col colone ">
             <img class="img" src="~@/assets/bedroom.jpg">
            </div>
            <div class="col coltwo ">
            <h5>Member Rate Summer Sale</h5>
            <ul>
              <li>Includes buffet breakfast for 1 guest per person daily at Papillon restauran</li>
              <li>20 percent off Flexible Rate</li>
              <li>See Rate details</li>
              <p><a href="#">Rate Details</a></p>
            </ul>
            </div>
            <div class="col colthree ">
             <p class="price"><span class="large"><b>120</b></span>USD/night</p>
            </div>
             <div class="col colfour ">
             <button class="btn btn-dark" @click="$router.push('checkout')">SELECT</button>
            </div>
    </div>
    </div>



    <div class="container mobileview">
     
        <div >
            <div class="colone ">
             <img class="img" src="~@/assets/bedroom.jpg">
              <h1>Superior King Room, Guest room, 1 King, City view, Corner room, Mid floor, Balcony</h1>
              <p><a href="#">Room Details</a></p>
            </div>
            <div class="coltwo">
              <hr>
            <h5>Member Rate Summer Sale</h5>
            <ul>
              <li>Includes buffet breakfast for 1 guest per person daily at Papillon restauran</li>
              <li>20 percent off Flexible Rate</li>
              <li>See Rate details</li>
              <p><a href="#">Rate Details</a></p>
            </ul>
            </div>
            <div class="colthree ">  
             
             <p class="price"><span class="large"><b>120</b></span>USD/night</p>
             <button class="btn btn-dark" @click="$router.push('checkout')">SELECT</button>
             
            
            </div>
        
    </div>
    </div>
    </section>
</template>

<script>


export default{
    name: 'Reservation',
    components:{

    }
}
</script>


<style scoped>
.mobileview{
  display: none;
}
.webview{
  display: inline;
}

#reservation{
  margin-top: 50px;
}
.container{
  
  margin-top: 50px;
}
.col{
  text-align: left;
}
h1{
  font-size: 27px;
  font-weight: bold;
  line-height: 2;
}
.img{
  width: 250px;
  height: 180px;
}
.btn{
  position: absolute;
  top: 50%;
  width: 200px;
  height: 45px;
}
.price{
  position: absolute;
  top: 50%;
}
.large{
  font-size: 40px;
}
 
/* mobile-view */
@media (max-width: 320px){
#reservation{
  text-align:left;
}
.mobileview{
  display: inline;
}
.webview{
  display: none;
}
h1{
  font-size: 16px;
  line-height: 1;
}
.btn{
  position: relative;
  width: 100px;
  left: 50px;
 
}

.price{
  position: relative;
  top: 10px;
  
}
.colthree{
  display: flex;
}
.large{
  font-size: 30px;
}

}

</style>
