<template>
  <FormulateForm
      class="registration-container pb-6"
      v-model="formValues"
      @submit="submitHandler"
      #default="{ isLoading }"
  >

    <div v-show="step === 1">
      <StepOne :form-values="formValues"/>
      <NextButton @next="next()"/>
    </div>

    <div v-show="step === 2">
      <StepTwo :form-values="formValues"/>
      <div class="registration-btn-wrapper">
        <PreviousButton @prev="prev()"/>
        <NextButton @next="next()"/>
      </div>
    </div>

    <div v-show="step === 3">
      <StepThree :form-values="formValues"/>
      <div class="registration-btn-wrapper">
        <PreviousButton @prev="prev()"/>
        <NextButton @next="next()"/>
      </div>
    </div>

    <div v-show="step === 4">
      <StepFour :form-values="formValues"/>
      <PreviousButton @prev="prev()"/>

      <FormulateInput
          type="submit"
          :disabled="isLoading"
          :label="isLoading ? 'Loading...' : 'Submit this form'"
      />
    </div>

    <pre
        class="code"
        v-text="formValues"
    />

  </FormulateForm>
</template>

<script>
import StepOne from "./StepOne";
import StepTwo from "./StepTwo";
import StepThree from "./StepThree";
import StepFour from "./StepFour";
import PreviousButton from "./PreviousButton";
import NextButton from "../../NextButton";
import axios from "axios";
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
      formValues: {}
    }
  },
  methods: {
    prev() {
      this.step--;
    },
    next() {
      this.step++;
    },
    async submitHandler (data) {
      console.log(data);

      // not a parent
      if(data.profileType !== "parent"){
        data.parentEmail = false
      }
      await axios.post('https://hookb.in/6JlDz7LKwGhoRnwwRZNW', data)
          .then(response => console.log(response))

    }
  }
}
</script>

<style scoped>
.registration-btn-wrapper{
  @apply flex p-6 justify-between;
}
</style>