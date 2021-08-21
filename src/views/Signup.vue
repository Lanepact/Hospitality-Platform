<template>
  <div class="signin container">
    <!-- <h1 class="fw-bold">Welcome and enjoy the beautiful view</h1> -->
    <div class="p-3 mt-4">
      <h2 class="fw-bold">SIGN UP</h2>
      <div class="signin-container d-flex space-between w-100">
        <form class="ms-4 m-4 w-100" >
          <div class="mb-3 d-flex w-100">
            <div class="w-50">
              <label for="signupFirstName" class="form-label">First Name</label>
              <Input type="text" class="form-control p-3 w-75 fw-bold" id="signupFirstName" aria-describedby="emailHelp"/>
            </div>
            <!-- <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div> -->
            <div class="w-50">
              <label for="signupLastName" class="form-label">Last Name</label>
              <Input type="text" class="form-control p-3 w-75 fw-bold" id="signupLastName" aria-describedby="emailHelp"/>
            </div>
          </div>
          <div class="mb-3 d-flex w-100">
            <div class="w-50">
              <label for="signupEmail" class="form-label">Email Address</label>
              <Input type="email" class="form-control p-3 w-75 fw-bold" id="signupEmail" aria-describedby="emailHelp"/>
            </div>
            <!-- <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div> -->
            <div class="w-50">
              <label for="signupPhoneNumber" class="form-label">Phone Number</label>
              <Input type="phone" class="form-control p-3 w-75 fw-bold" id="signupPhoneNumber" aria-describedby="emailHelp"/>
            </div>
          </div>
          <div class="mb-3 d-flex w-100">
            <div class="w-50">
              <label for="signupPassword" class="form-label">Password</label>
              <Input type="password" class="form-control p-3 w-75 fw-bold" id="signupPassword" aria-describedby="emailHelp"/>
            </div>
            <!-- <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div> -->
            <div class="w-50">
              <label for="signupLastName" class="form-label">Confirm Password</label>
              <Input type="password" class="form-control p-3 w-75 fw-bold" id="signupConfirmPassword" aria-describedby="emailHelp"/>
            </div>
          </div>
          <div class="mb-3 form-check">
            <Input type="checkbox" class="form-check-input" id="rememberMe" />
            <label class="form-check-label" for="rememberMe">Remember Me</label>
          </div>
          <div class="mb-3 form-check">
            <Input type="checkbox" class="form-check-input" id="termsAndConditions" />
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
import Input from "@/components/Input";
import Button from "@/components/Button";
// import Images  from "@/components/Images";
import hotelImage from "@/assets/hotel1.jpg";

export default {
  name: 'Signin',
  components: {
    Input,
    Button
  },
  data() {
    return {
      hotelImage: hotelImage
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