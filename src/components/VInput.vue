<template>
  <label>
    {{ label }}
    <input v-if="type !== 'select'"
      :type="type"
      v-model="inputValue"
      :placeholder="holder"
    >

    <select v-else>
      <option
        v-for="(option, i) of options"
        :key="i"
        :value="option.value"
      >
        {{ option.content }}
      </option>
    </select>
  </label>
</template>

<script>
export default {
  name: 'VInput',
  props: {
    label: String,
    type: {
      type: String,
      required: true
    },
    holder: String,
    options: Array,
    modelValue: String
  },
  computed: {
    inputValue: {
      get () {
        return this.modelValue
      },
      set (value) {
        this.$emit('update:modelValue', value)
      }
    }
  }
}
</script>

<style scoped lang="scss">

</style>
