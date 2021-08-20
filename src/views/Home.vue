<template>
  <div class="home" id="home">
    <Banner banner-text="PROFILE SETUP"/>
    <FormWrapper/>
    <div id="thick-rule" class="bg-energetic-blue h-6 my-16"></div>
    <ContactUs/>
    <Footer/>
  </div>
</template>

<script>
import Banner from "../components/Banner";
import Footer from "../components/Footer";
import ContactUs from "../components/ContactUs";
import FormWrapper from "../components/FormWrapper";

export default {
  name: 'Home',
  components: {
    Banner,
    Footer,
    ContactUs,
    FormWrapper
  }
}
</script>