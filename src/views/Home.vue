<template>
  <div class="home">
    <Main/>
    <Information/>
    <Carousel/>
    <Info/>
    <Carouseltwo/>
    <Infotwo/>
    <Card/>
    <Footer/>
  </div>
</template>

<script>
// @ is an alias to /src
import Carousel from "@/components/Carousel";
import Main from "@/components/Main";
import Information from "@/components/Information";
import Info from "@/components/Info";
import Carouseltwo from "@/components/Carouseltwo";
import Infotwo from "@/components/Infotwo";
import Card from "@/components/Card"
import Footer from "@/components/Footer"



export default {
  name: 'Home',
  components: {
    Carousel,
    Main,
    Information,
    Info,
    Carouseltwo,
    Infotwo,
    Card,
    Footer
   
  }
}
</script>
