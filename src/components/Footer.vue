<template>
    <section id="footer">
        <hr>
        <div class="container">   
  <div class="row">
    <div class="col links col-sm-3" >
      <ul>
          <li><a href="#">SHERATON STORE</a></li>
          <li><a href="#">VACATION CLUB</a></li>
          <li><a href="#">NEWS</a></li>
          <li><a href="#">CAREERS</a></li>
          <li><a href="#">DEVELOPERS</a></li>
          <li><a href="#">TRAVEL PROFESSIONALS</a></li>
          <li><a href="#">MEETINGS</a></li>

      </ul>
    </div>
    <div class="col ">
      <h2>STAY CONNECTED</h2>
      <div class="footericons">
      <i class="fab fa-twitter footer-icon fa-2x"></i>
      <i class="fab fa-instagram footer-icon fa-2x"></i>
      <i class="fab fa-facebook-f footer-icon fa-2x"></i>
      <i class="fab fa-youtube footer-icon fa-2x"></i>
   </div>
    </div>
    <div class="col ">
     <Images :source="devices"/>
        <div class="container">
  <div class="row">
    <div class="col">
      <pre>
    Explore The Possibilities
    What you need,
    When you need it.</pre>
     <button type="button" class="btn ">LEARN MORE</button>
    </div>
    <div class="col download-buttons ">
    <button type="button" class="btn btn-dark btn-lg download-btn download-btn-one"><i class="fab fa-apple"></i>Download</button>
    <button type="button" class="btn btn-light btn-lg download-btn download-btn-two"><i class="fab fa-google-play"></i>Download</button>
    </div>
  </div>
</div>


    </div>
  </div>
</div>
    </section>
</template>

<script>
    import Images  from "@/components/Images"
    import devices from "@/assets/devices.png"
export default{
    name:'Footer',
    components:{
        Images,
    },
    data(){
    return{
        devices:devices
    }
}
}

</script>

<style scoped>
    #footer{
        background-color: #3a3a3a;
        color: white;
        padding-top:50px ;
    }
    li{
        list-style: none;
    }
    a{
        text-decoration: none;
        color: white;
        line-height: 3;
    }
    .footer-icon{
    margin: 20px 10px;
}
hr{
    border-bottom: 50px;
    color: #000000;
    width: 90%;
    margin-left: 70px;
}
pre{
    text-align: left;
    margin-left:0;
}
.btn{
    text-align: center;
    background-color: bisque;
    border: none;
    margin: 20px;
}

.download-btn-one{
    text-align: center;
    background-color: black;
    color: white;
    border: none;
    margin: 10px;
}

.download-btn-two{
    text-align: center;
    background-color: black;
    color: white;
    border: none;
    margin: 10px;
}
@media (max-width: 500px){
    .download-btn-one{
    text-align: center;
    background-color: black;
    color: white;
    border: none;
    margin: 10px;
    width:200px;
}

.download-btn-two{
    text-align: center;
    background-color: black;
    color: white;
    border: none;
    margin: 10px;

}
}
/* tablets */
@media (max-width: 800px){
   .links{
       padding-right:50%;
   } 
    .download-btn-one{
    text-align: center;
    background-color: black;
    color: white;
    border: none;
    /* margin: 10px; */
    width:200px;
}

.download-btn-two{
    text-align: center;
    background-color: black;
    color: white;
    border: none;
    width: 200px;
    /* margin: 10px; */

}
}
</style>