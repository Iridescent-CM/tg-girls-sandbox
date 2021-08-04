<template>
  <div class="container mx-auto max-w-2xl border-energetic-blue rounded-md">
    <div class="energetic-blue">
      <h4 class="text-left font-extrabold p-4 text-white"> Your Profile Type</h4>
    </div>
    <FormulateForm  @submit="submitted" class="p-8">
      <h2 class="text-2xl mb-2 text-left font-semibold">I am a...</h2>
      <FormulateInput
          label-position="before"
          type="radio"
          class="profile-type"
          :options="options"

      />
      <FormulateInput
          input-class="px-4 py-2 rounded bg-green-500 text-white hover:bg-green-600"
          type="submit"
      />
<!--      <pre class="mt-8 p-2 bg-gray-200 whitespace-pre text-sm">{{ values }}</pre>-->
    </FormulateForm>

  </div>

</template>


<script>
export default {
  name: 'RegistrationForm',
  data() {
    return {
      values: {},
      options: [
        {
          label: `<img src="${require('../assets/myTG-parent.png')}" alt=""> <span class="label-text">PARENT <br> Registering a daughter 8-12 years old</span>`,
          value: "parent",
        },
        {
          label: `<img src="${require('../assets/myTG-student.png')}" alt=""><span class="label-text"> STUDENT <br> 13 - 18 year old female-identifying student</span>`,
          value: "student",
        },
        {
          label: `<img src="${require('../assets/myTG-mentor.png')}" alt=""> <span class="label-text">MENTOR <br> Over 18 years old who wants to help guide a team of girls</span>`,
          value: "mentor",
        }
      ],
    };
  },
}
</script>

<style>
/*.formulate-input-group {*/
/*  display: flex;*/
/*  justify-content: space-evenly;*/
/*}*/
/*.profile-type img {*/
/*  width: 7em;*/
/*  !*margin-right: 0.5em;*!*/
/*  margin: auto;*/
/*}*/

/*[data-classification="box"] .formulate-input-wrapper {*/
/*  display: flex;*/
/*  align-items: center;*/
/*}*/



/*HORIZONTAL RADIO BUTTONS*/
.formulate-input-group-item {
  display: flex;
}
.profile-type img {
  width: 7em;
  margin-left: 1rem;
  margin-right: 1.5rem;
}

[data-classification="box"] .formulate-input-wrapper {
  display: flex;
  align-items: center;
}

.radio-label{
  display: flex;
  align-items: center;
}

.label-text{
  text-align: left;
}




</style>