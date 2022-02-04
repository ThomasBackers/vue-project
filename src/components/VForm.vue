<template>
  <form action="" method="post">
    <img
      v-if="logo"
      :src="logo"
      alt=""
    >

    <h3 v-if="heading">
      {{ heading }}
    </h3>

    <VInput
      v-for="(input, i) of inputs"
      :key="i"
    >
  </form>
</template>

<script>
import VInput from '@/components/VInput.vue'

export default {
  name: 'VForm',
  components: {
    VInput
  },
  props: [
    'logo',
    'heading',
    'inputs'
  ]
}
</script>

<style scoped lang="scss">

</style>
