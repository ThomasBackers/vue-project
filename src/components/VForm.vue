<template>
  <form :action="action" :method="method">
    <img
      v-if="icon"
      :src="require('../assets/' + icon)"
      alt="form icon"
    >

    <h3 v-if="heading">
      {{ heading }}
    </h3>

    <VInput
      v-for="(input, i) of inputs"
      :key="i"
      :label="input.label"
      :type="input.type"
      v-model="input.value"
    />
  </form>
</template>

<script>
import VInput from '@/components/VInput.vue'

export default {
  name: 'VForm',
  components: {
    VInput
  },
  props: {
    action: String,
    method: String,
    icon: String,
    heading: String,
    inputs: Array
  }
}
</script>

<style scoped lang="scss">

</style>
