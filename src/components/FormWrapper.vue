<template>
  <FormulateForm class="registration-container pb-6"  @submit="submitted" >

    <div v-show="step === 1">
      <StepOne/>
      <button @click.prevent="next()" class="px-4 py-2 rounded bg-green-500 text-white hover:bg-green-600">Next</button>
    </div>

    <div v-show="step === 2">
      <StepTwo/>
      <button @click.prevent="prev()" class="px-4 py-2 rounded bg-green-500 text-white hover:bg-green-600">Previous</button>
      <button @click.prevent="next()" class="px-4 py-2 rounded bg-green-500 text-white hover:bg-green-600">Next</button>
    </div>

  </FormulateForm>
</template>

<script>
import StepOne from "./StepOne";
import StepTwo from "./StepTwo";
export default {
  name: "FormWrapper.vue",
  components:{
    StepOne,
    StepTwo
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

</style>