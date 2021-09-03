<template>
  <div class="signin container">
    <h1 class="fw-bold">Welcome and enjoy the beautiful view</h1>
    <div class="p-3 mt-4">
      <h2 class="fw-bold">SIGN IN</h2>
      <div class="signin-container d-flex space-between w-100">
        <form class="w-50 ms-4 mt-4" @submit.prevent="signIn">
          <div class="mb-3">
            <label for="signinEmail" class="form-label">Email address</label>
            <input v-model="email" type="email" class="form-control p-3 w-75 fw-bold" id="signinEmail" aria-describedby="emailHelp">
            <!-- <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div> -->
          </div>
          <div class="mb-3">
            <label for="signinPassword" class="form-label">Password</label>
            <input v-model="password" type="password" class="form-control p-3 w-75 fw-bold" id="signinPassword" >
          </div>
          <div class="mb-3 form-check">
            <input type="checkbox" class="form-check-input" id="rememberMe" >
            <label class="form-check-label" for="rememberMe">Remember Me</label>
          </div>
          <Button buttonType="submit" text="Sign In" class="btn p-2 fw-bold text-light fs-4"/>
          
        </form>
        <div class="d-flex flex-column">
          <Images :source="hotelImage" class="img-fluid border"/>
          <ul class="m-3">
            <li>Enjoy our lowest rates, all the time</li>
            <li>Free in-room Wi-Fi</li>
            <li>Mobile check-in and more</li>
          </ul>
          <router-link to="/signup"><Button class="w-100 btn p-3 fs-4 border border-dark" color="transparent" text="JOIN NOW" /></router-link>
          <router-view/>
        </div>
      </div>
    </div>
  </div>
  
</template>

<script>
import Button from "@/components/Button";
import Images  from "@/components/Images";
import hotelImage from "@/assets/hotel1.jpg";
import axios from 'axios';

export default {
  name: 'Signin',
  components: {
    Images,
    Button
  },
  data() {
    return {
      hotelImage: hotelImage,
      email: "",
      password: "",
      formInput: {},
      data: []
    }
  },
  methods: {
    signIn() {
      this.formInput = {
        email: this.email,
        password: this.password
      }

      axios.post('https://hospitalitybase.herokuapp.com/api/v1/users/login', this.formInput)
        .then(responce => {
          this.data = responce.data;
          console.log(this.data)
          
        })
        .catch(err => {
          console.log(err)
        })
    }
  }
}
</script>

<style scoped>
  .btn {
    width: 200px;
    background-color: #444054;
    box-shadow: 0 2px 4px 0 rgba(0,0,0,.3),0 4px 4px 0 rgba(0,0,0,.3);
  }
</style>