<template>
  <form :action="action" :method="method" @submit.prevent="handleSubmit">
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
      :holder="input.holder"
      :options="input.options"
      v-model="input.value"
    />

    <button>
      submit
    </button>
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
    action: {
      type: String,
      default: ''
    },
    method: {
      type: String,
      default: 'post'
    },
    icon: String,
    heading: String,
    inputs: {
      type: Array,
      required: true
    }
  },
  methods: {
    handleSubmit () {
      this.inputs.forEach(input => console.log(input.value))
    }
  }
}
</script>

<style scoped lang="scss">

</style>
