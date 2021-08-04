<template>
  <div class="registration-container" id="step-two">
    <ContainerHeader header-text="Basic Profile"/>
    <FormulateForm
        class="login-form"
        v-model="formValues"
    >
      <div id="student-information">
        <h2 class="registration-title">Student Information</h2>

        <div class="formulate-input-wrapper name-group">
          <FormulateInput
              name="first-name"
              type="text"
              label="First Name"
              placeholder="First Name"
              validation="required"
              class="flex-grow pr-2"
          />

          <FormulateInput
              name="last-name"
              type="text"
              label="Last Name"
              placeholder="Last Name"
              validation="required"
              class="flex-grow pl-2"

          />
        </div>

        <FormulateInput
            type="date"
            name="birthday"
            label="Birthday"
            placeholder="Student Birthday"
            error-behavior="live"

        />

        <FormulateInput
            name="school-name"
            type="text"
            label="School Name"
            placeholder="School Name"
            validation="required"
        />
      </div>


      <div id="parent-information">
        <h2 class="registration-title">Parent Information</h2>

        <div class="formulate-input-wrapper name-group">
          <FormulateInput
              name="parent-first-name"
              type="text"
              label="First Name"
              placeholder="Parent First Name"
              validation="required"
              class="flex-grow pr-2"
          />

          <FormulateInput
              name="parent-last-name"
              type="text"
              label="Last Name"
              placeholder="Parent Last Name"
              validation="required"
              class="flex-grow pl-2"
          />
        </div>

        <FormulateInput
            name="parent-email"
            type="email"
            label="Email Address"
            placeholder="Parent Email address"
            validation="required|email"
        />
      </div>

      <FormulateInput
          name="technovation-hear-about"
          type="text"
          label="How did you hear about Technovation? (Optional)"
      />

      <FormulateInput
          type="submit"
          label="Register"
      />
      <pre
          class="code"
          v-text="formValues"
      />
    </FormulateForm>

  </div>
</template>

<script>
import ContainerHeader from "./ContainerHeader";
export default {
  name: "StepTwo",
  components: {ContainerHeader}
}
</script>

<style scoped>
.login-form {
  padding: 2em;
}

.login-form::v-deep .formulate-input .formulate-input-element {
  max-width: none;
}


/*@media (min-width: 420px) {*/
/*  .double-wide {*/
/*    display: flex;*/
/*  }*/
/*  .double-wide .formulate-input {*/
/*    flex-grow: 1;*/
/*    width: calc(50% - .5em);*/
/*  }*/
/*  .double-wide .formulate-input:first-child {*/
/*    margin-right: .5em;*/
/*  }*/
/*  .double-wide .formulate-input:last-child {*/
/*    margin-left: .5em;*/
/*  }*/
/*}*/
</style>