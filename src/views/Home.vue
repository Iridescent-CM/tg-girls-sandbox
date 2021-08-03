
<template>
  <div class="home" id="home">
    <Banner/>
    <HelloWorld msg="Technovation Girls Registration"/>
    <ContactUs/>
    <Footer/>
  </div>
</template>

<script>
import HelloWorld from '../components/HelloWorld.vue'
import Banner from "../components/Banner";
import Footer from "../components/Footer";
import ContactUs from "../components/ContactUs";


export default {
  name: 'Home',
  components: {
    HelloWorld,
    Banner,
    Footer,
    ContactUs,
  }
}
</script>

<style>
#home2 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>















<!--<template>-->
<!--  <div class="home">-->
<!--    <img alt="Vue logo" src="../assets/logo.png">-->
<!--    <HelloWorld msg="Welcome to Your Vue.js App"/>-->
<!--  </div>-->
<!--</template>-->

<!--<script>-->
<!--// @ is an alias to /src-->
<!--import HelloWorld from '@/components/HelloWorld.vue'-->

<!--export default {-->
<!--  name: 'Home',-->
<!--  components: {-->
<!--    HelloWorld-->
<!--  }-->
<!--}-->
<!--</script>-->
