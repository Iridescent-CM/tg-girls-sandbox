<template>
  <div class="tg-green-stripes rubik h-36 flex items-center mb-20">
    <div class="text-white sm:ml-8 lg:ml-72 text-7xl font-black">{{ bannerText }}</div>
  </div>
</template>

<script>
export default {
  name: 'Banner',
  props: {
    bannerText: String
  }
}
</script>