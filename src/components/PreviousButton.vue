<template>
  <button @click.prevent="$emit('prev')" class="registration-btns">Previous</button>
</template>

<script>
export default {
  name: "PreviousButton",
}
</script>

<style scoped>

</style>