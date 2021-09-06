<template>
  <section id="checkout">
    <div class="heading">
      <h2>Guest Information</h2>
      <button class="btn btn-block btn-dark btnone">SIGN IN FOR FASTER BOOKING</button>
    </div>
    <hr>
    <div>
      <p>All fields are required unless otherwise stated.</p>
    <div class="name-form">
        <h2>Name</h2>
        <form>
          <div>
          <label for="title">Title</label>
         <select class="form-select">  
         <option selected>(optional)</option>
         <option value="1">Mr</option>
        <option value="2">Mrs </option>
        <option value="3">Miss</option>
        </select>
        <br>
        </div>
          <div class="row g-3 align-items-left">
        <div class="col-auto">
          <label for="title">Firstname</label>
        <input type="text" id="fname" class="form-control input-box" >
      </div>
      <div class="col-auto">
          <label for="title">Lastname</label>
        <input type="text" id="lname" class="form-control input-box"  >
      </div>
          </div>
          <br>
       <div>
         <label for="title">Email</label>
        <input type="text" id="email" class="form-control lg-input"  >
       </div>
        <br>
       <div>
         <label for="title">Marriott Bonvoy Member Number (Optional)</label>
        <input type="text" id="membernum" class="form-control lg-input"  >

       </div>
       <br>
         <div>
         <label for="title">Company Name</label>
        <input type="text" id="company" class="form-control lg-input"  >
       </div>

        <p>Note: To be credited for this stay, the name on your Marriott Bonvoy account must match the guest name.</p>
        <br>
        <div class="address-form">
        <h2>Address</h2>
        <br>
          <div>
          <label for="title">Country/Region</label>
         <select class="form-select">  
         <option selected>USA</option>
         <option value="1">Nigeria</option>
        <option value="2">Algeria</option>
        <option value="3">Canada</option>
        </select>
        </div>
</div>
<br>
        <div>
         <label for="title">Address</label>
        <input type="text" id="address" class="form-control lg-input">
        <br>
        <input type="text" id="addresstwo" class="form-control lg-input" >
       </div>
<br>
        <div>
         <label for="title">City</label>
        <input type="text" id="city" class="form-control lg-input"  >
       </div>
       <br>

      <div class="row g-3 align-items-center">
        <div class="col-auto">
          <label for="title">State/province</label>
        <input type="text" id="fname" class="form-control input-box" >
      </div>
      <div class="col-auto">
          <label for="title">zip code</label>
        <input type="text" id="lname" class="form-control input-box"  >
      </div>
          </div>
          <hr>
          <div>
          <h3>Select payment option</h3>
         <p> A valid form of payment must be presented at check-in</p>
         </div>

      

         <div>
           <p>Free Wi-Fi + mobile check-in + our lowest member rates all the time</p>
         </div>
         <span>
           <input type="checkbox" name="marriott">
           <label for="marriott" class="label-text">Instantly join Marriott Bonvoy and enjoy the perks with each stay.</label>
         </span>

        <br>

         <div>
         <label for="password">Password</label>
        <input type="password" id="password" class="form-control sm-input"  >
       </div>
       <br>
        <div>
         <label for="confirm">Confirm password</label>
        <input type="password" id="confirm" class="form-control sm-input"  >
       </div>
       <hr>

        <span>
           <input type="checkbox" name="marriott">
           <label for="marriott" class="label-text">I would like to receive exclusive offers from select third parties.</label>
         </span>
          <br>
         <span>
           <input type="checkbox" name="marriott">
           <label for="marriott" class="label-text">I would like to receive account updates, program news and offers via email and direct mail.</label>
         </span>
          <br><br>
         <p>By signing up, I agree to Marriott's Terms of Use, Privacy Statement and Data Protection Clause.</p>
          <br><br>
          <p>You may cancel your reservation for no charge until 6:00 PM hotel time on September 1, 2021. Please note that we will assess a fee of 162.33 USD if you must cancel after this deadline. If you have made a prepayment, we will retain all or part of your prepayment. If not, we will charge your credit card.</p>

          <a href="#">Learn more</a>
          <br><br>

            <button class="btn-block btn-lg btn-dark btn-two">BOOK NOW</button>

        </form>

    </div>
    </div>

  </section>
</template>


<script>

export default{
    name: 'Checkout',
    components:{
      
    },
     
  }

</script>

<style scoped>
#checkout{
  margin: 100px;
}
p{
  text-align: left;
}
form{
 padding-top: 20px;
}

.btnone{
  height: 70px;
}

.heading{
  text-align:left;
  
}
.double{
  margin: 0;
}

.form-select{
  width: 30%;
  height: 50px;
}
.input-box{
  width: 500px;
  height: 50px;
}
.name-form{
  text-align: left;
}
.lg-input{
  width:90% ;
  height: 50px;
}
.sm-input{
  width: 30%;
  height: 50px;
}
input[type="checkbox"]{
  display: inline;
  width: 30px;
  height: 20px;
 
}
.label-text{
  display: inline-block;
  padding: 5px;
}
.btn-two{
  width: 70%;
  height: 70px;
}


 
/* mobile-view */
@media (max-width: 320px){
  #checkout{
    margin: 10px;
  }
  .btn{
    height: 50px;
    width: 280px;
    text-align: left;
  }
  p{
    text-align: left;
  }

  .form-select{
  width: 270px;
  height: 50px;
}

.lg-input{
  width:270px ;
  height: 50px;
}
.input-box{
   width:270px;
  height: 50px;
}
.sm-input{
  width: 270px;
  height: 50px;
}

.btn-two{
  width: 270px;
  height: 50px;
}

p{
  text-align: left;
} 

}
</style>