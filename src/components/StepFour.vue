<template>

  <div id="step-four">
    <ContainerHeader header-text="Set your email and password"/>

    <div id="email-password" class="form-wrapper">
      <h1 class="text-tg-green text-2xl text-left mb-6">This is an account for ________ division</h1>

<!--      <h2 class="registration-title">Email Address</h2>-->
      <FormulateInput
          name="email"
          type="email"
          label="Email Address"
          placeholder="Email address"
          validation="required|email"
          class="flex-grow"
      />

      <p class="text-left text-sm mb-12">Please choose a personal, permanent email. A school or company email might block us from sending important messages to you.</p>

      <div class="double-wide">

<!--        <h2 class="registration-title">Password</h2>-->

        <FormulateInput
            name="password"
            type="password"
            label="Password"
            placeholder="At least 8 characters"
            validation="required"
        />
      </div>

    </div>

  </div>

</template>

<script>
import ContainerHeader from "./ContainerHeader";
export default {
  name: "StepFour",
  components: {
    ContainerHeader
  }
}
</script>

<style scoped>
</style>