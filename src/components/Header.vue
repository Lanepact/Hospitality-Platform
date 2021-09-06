<template>
  <div id="nav">
    <router-link class="
    nav-item" to="/">Home</router-link> 
    <router-link class="
    nav-item" to="/signin">SignIn</router-link>
    <Button text="Reserve Now" class="btn p-2 text-bold" type="button" data-bs-toggle="modal" data-bs-target="#exampleModal" @click="$router.push('reservation')" />
    <Modal class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
      <form>
        <div class="mb-3 d-flex w-100">
          <div class="w-50 m-2">
            <div>
              <label for="signupFirstName" class="form-label">Rooms</label>
              <div class="border border-1 h-auto p-2">
                <input class="w-75 " type="text" :placeholder="roomCounter.value + ' Rooms'" >
                <Button type="button" text="-" @click="add()" />
                <Button type="button" text="+" />
              </div>
            </div>
            <div>
              <label for="signupFirstName" class="form-label">Guests</label>
              <div class="border border-1 h-auto p-2">
                <input class="w-75 " type="text"  >
                <Button text="-" class="p-2 m-2"/>
                <Button text="+" class="p-2 m-2"/>
              </div>
            </div>
          </div>
          <div class="w-50 m-2">
            <div>
              <label for="signupFirstName" class="form-label">Stay Dates</label>
              <div class="border border-1 h-auto p-2 d-flex justify-content-evenly">
                <input class="w-75 " type="date"  >
                <input class="w-75 " type="date"  >
              </div>
            </div>
          <Button class="mt-4 w-100 p-2 text-bold btn" text="Book Room" />
          </div>
        </div>
      </form>
    </Modal>
  </div>
  <router-view/>
</template>

<script>
import  Button  from "@/components/Button";
import Modal from "@/components/Modal";
import { ref } from '@vue/reactivity';


export default {
  name: 'App',
  components: {
    Button,
    Modal,
    
  },
  setup() {
    let roomCounter = ref(0);

    const add = () => {
      roomCounter.value += 1;
      console.log(roomCounter.value)
    }



    return {
      add, roomCounter
    }
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

  .pill {
    border-radius: 50%;
  }
</style>