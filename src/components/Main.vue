<template>
    <section id="main-content">
    <div class="message">
        <h2>Where the world comes together</h2>
    </div>

    <div class="container main-form">
        <div class="row">
            <div class="col">
                <h3 class="form-content">Explore the world</h3>
            </div>
  <div class="col form-content">
      <label for="" >DESTINATION</label>
    <input type="text" class="form-control" placeholder="First name" aria-label="First name">
  </div>
  <div class="col form-content">
      <label for="">STAY DATES</label>
    <input type="text" class="form-control" placeholder="Last name" aria-label="Last name">
  </div>
  <div class="mobile-view">
    <input type="text" placeholder="Where to?">
      <Button text="Reserve" class="btn p-2 text-bold" type="button" data-bs-toggle="modal" data-bs-target="#exampleModal" />
    <Modal class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true"/>
  </div>
  <div class="col form-content">
      <Button text="HOTEL SEARCH" class="btn p-2 text-bold" type="button" data-bs-toggle="modal" data-bs-target="#exampleModal" />
    <Modal class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
      <form>
        <div class="w-50">
            <label for="signupFirstName" class="form-label">Destination</label>
            
          </div>
          <div class="w-50">
            <label for="signupLastName" class="form-label">Last Name</label>
            <Input type="text" class="form-control p-3 w-75 fw-bold" id="signupLastName" aria-describedby="emailHelp"/>
          </div>
      </form>
    </Modal>
  </div>
</div>
    </div>
</section>
</template>


<script>
import  Button  from "@/components/Button";
import Modal from "@/components/Modal";


export default{
    name:'Main',
    components: {
    Button,
    Modal
  }
}
</script>

<style scoped>
/* 
main content styles */
#main-content{
    background: url('~@/assets/main.jpg') no-repeat center ;
    background-size: cover;
    /* padding: 10%; */
    padding: 3% 15% 7%;
    height: 100%;
}
.message{
    text-align: center;
    background-color:rgba(245, 245, 245, 0.685);
    width:30%;
    margin-left: 0;
    margin-top: 10%;
    margin-bottom: 30%;
    padding:15px;
}
.main-form{
    background-color:#fff;
    width: 100%;
    padding:3%;
    padding-bottom: 3%;
    margin-bottom: 0;
}
.btn{
    text-align: center;
    background-color: bisque;
    border: none;
    margin: 20px;
}
.mobile-view{
  display: none;
}

/* mobile view */
@media (max-width: 500px) {
  .message{
    text-align: center;
    background-color:linen;
    width:90%;
    position: relative;
    top: 300px;
    margin-right:10%;
    margin-left: 10%;
    margin-top: 50%;
    margin-bottom: 30%;
    padding:19px;
}

.main-form{
   position: relative;
   top: 200px;
   /* z-index: ; */
  text-align: center;
  padding-top:20px;
  
  
}
input{
  width: 200px;
 
}
.mobile-view{
  display: inline;
   padding: 0;
}
.form-content{
  display: none;
}
.btn{
  text-align: center;
  height: 34px;
}
}
/* tablets */
@media (max-width: 800px) {
  .message{
    text-align: center;
    background-color:linen;
    width:90%;
    position: relative;
    top: 320px;
    margin-right:10%;
    margin-left: 10%;
    margin-top: 50%;
    margin-bottom: 30%;
    padding:19px;
}

.main-form{
   position: relative;
   top: 200px;
   /* z-index: ; */
  text-align: center;
  padding-top:20px;
  padding-bottom: 10px;
  
}
input{
  width: 200px;
 
}
.mobile-view{
  display: inline;
   padding: 0;
}
.form-content{
  display: none;
}
.btn{
  text-align: center;
  height: 34px;
}
}

</style>