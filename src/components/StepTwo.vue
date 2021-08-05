<template>
  <div id="step-two">
    <ContainerHeader header-text="Basic Profile"/>

    <div id="student-information" class="form-wrapper">

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

    <div id="parent-information" class="form-wrapper">
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

      <FormulateInput
          name="technovation-hear-about"
          type="text"
          label="How did you hear about Technovation? (Optional)"
      />

      <pre
          class="code"
          v-text="formValues"
      />

    </div>
  </div>
</template>

<script>
import ContainerHeader from "./ContainerHeader";
export default {
  name: "StepTwo",
  components: {ContainerHeader},
}
</script>

<style scoped>
  .login-form {
    padding: 2em;
  }

  .login-form::v-deep .formulate-input .formulate-input-element {
    max-width: none;
  }
</style>