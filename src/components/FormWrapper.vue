<template>
  <FormulateForm class="registration-container pb-6"  @submit="submitted" >

    <div v-show="step === 1">
      <StepOne/>
      <NextButton @next="next()"/>
    </div>

    <div v-show="step === 2">
      <StepTwo/>
      <div class="registration-btn-wrapper">
        <PreviousButton @prev="prev()"/>
        <NextButton @next="next()"/>
      </div>
    </div>

    <div v-show="step === 3">
      <StepThree/>
      <div class="registration-btn-wrapper">
        <PreviousButton @prev="prev()"/>
        <NextButton @next="next()"/>
      </div>
    </div>

    <div v-show="step === 4">
      <StepFour/>
      <PreviousButton @prev="prev()"/>
    </div>

  </FormulateForm>
</template>

<script>
import StepOne from "./StepOne";
import StepTwo from "./StepTwo";
import StepThree from "./StepThree";
import StepFour from "./StepFour";
import PreviousButton from "./PreviousButton";
import NextButton from "../../NextButton";
export default {
  name: "FormWrapper.vue",
  components:{
    StepOne,
    StepTwo,
    StepThree,
    StepFour,
    PreviousButton,
    NextButton
  },
  data(){
    return {
      step: 1,
    }
  },
  methods: {
    prev() {
      this.step--;
    },
    next() {
      this.step++;
    }
  }
}
</script>

<style scoped>
.registration-btn-wrapper{
  @apply flex p-6 justify-between;
}
</style>