<template>
  <div class="signin container">
    <!-- <h1 class="fw-bold">Welcome and enjoy the beautiful view</h1> -->
    <div class="p-3 mt-4">
      <h2 class="fw-bold">SIGN UP</h2>
      <div class="signin-container d-flex space-between w-100">
        <form class="ms-4 m-4 w-100" method="post" @submit.prevent="signup">
          <div class="mb-3 d-flex w-100">
            <!-- <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div> -->
            <div class="w-100">
              <label for="name" class="form-label">Full Name</label>
              <input v-model="name" type="text" class="form-control p-3 w-75 fw-bold" id="name" aria-describedby="emailHelp" required>
            </div>
          </div>
          <div class="mb-3 d-flex w-100">
            <div class="w-100">
              <label for="signupEmail" class="form-label">Email Address</label>
              <input v-model="email" type="email" class="form-control p-3 w-75 fw-bold" id="signupEmail" aria-describedby="emailHelp" required>
            </div>
            <!-- <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div> -->
            <!-- <div class="w-50">
              <label for="signupPhoneNumber" class="form-label">Phone Number</label>
              <Input type="phone" class="form-control p-3 w-75 fw-bold" id="signupPhoneNumber" aria-describedby="emailHelp"/>
            </div> -->
          </div>
          <div class="mb-3 d-flex w-100">
            <div class="w-50">
              <label for="signupPassword" class="form-label">Password</label>
              <input v-model="password" type="password" class="form-control p-3 w-75 fw-bold" id="signupPassword" aria-describedby="emailHelp" required>
              <p v-if="passwordError">{{passwordError}}</p>
            </div>
            <!-- <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div> -->
            <div class="w-50">
              <label for="signupConfirmPassword" class="form-label">Confirm Password</label>
              <input v-model="confirmPassword" type="password" class="form-control p-3 w-75 fw-bold" id="signupConfirmPassword" aria-describedby="emailHelp" required>
              <p v-if="passwordCountError">{{passwordCountError}}</p>
            </div>
          </div>
          <!-- <div class="mb-3 form-check">
            <Input v-model="rememberMe" type="checkbox" class="form-check-input" id="rememberMe" />
            <label class="form-check-label" for="rememberMe">Remember Me</label>
          </div> -->
          <div class="mb-3 form-check">
            <input v-model="terms" type="checkbox" class="form-check-input" id="termsAndConditions" required>
            <label class="form-check-label" for="termsAndConditions">I agree to the Terms and Conditions</label>
          </div>
          <Button buttonType="submit" text="JOIN" class="btn p-2 fw-bold text-light fs-4"/>
          <p></p>
        </form>
      </div>
    </div>
  </div>
  
</template>

<script>
import Button from "@/components/Button";
import hotelImage from "@/assets/hotel1.jpg";
import axios from 'axios';

export default {
  name: 'Signin',
  components: {
    Button,
  },
  data() {
    return {
      hotelImage: hotelImage,
      name: '',
      email: "",
      password: "",
      confirmPassword: "",
      passwordError: '',
      passwordCountError: '',
      terms: false,
      formInput: {}
    }
  },
  methods: {
    signup() {
      this.passwordError = this.password.length > 8 ? '' : 'Password must be more than 8 characters.'
      this.passwordCountError = this.password === this.confirmPassword ? '' : 'Password Incorrect'
      this.formInput = {
        name: this.name,
        email: this.email,
        password: this.password,
        passwordConfirm: this.confirmPassword
      }
      axios.post('https://hospitalitybase.herokuapp.com/api/v1/users/signup', this.formInput)
        .then(() => {
          alert('Thank you for signing up');
        })
        .catch(err => {
          console.log(err)
        })
    },
    reset(){
      this.formInput = { 
        name: "",
        email: "",
        password: "",
        passwordConfirm: ""
      }
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