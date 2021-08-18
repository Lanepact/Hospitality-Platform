<template>
  <div id="nav">
    <router-link class="
    nav-item" to="/">Home</router-link> 
    <router-link class="
    nav-item" to="/signin">SignIn</router-link>
    <Button text="Reserve Now" class="btn p-2 text-bold" type="button" data-bs-toggle="modal" data-bs-target="#exampleModal" />
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
  <router-view/>
</template>

<script>
import  Button  from "@/components/Button";
import Modal from "@/components/Modal";

export default {
  name: 'App',
  components: {
    Button,
    Modal
  }
}
</script>

<style scoped>
  #app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

#nav {
  padding: 30px;
  display: flex;
  justify-content: end;
}

.nav-item {
  padding: 3px;
  text-decoration: none;
  font-size: 1.4rem;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.btn {
    width: 300px;
    background-color: #f8dec3;
    box-shadow: 0 2px 4px 0 rgba(0,0,0,.3),0 4px 4px 0 rgba(0,0,0,.3);
  }
</style>