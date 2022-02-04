<template>
  <label>
    {{ label }}
    <input :type="type">
  </label>
</template>

<script>
export default {
  name: 'VInput',
  props: {
    label: String,
    type: String
  }
}
</script>

<style scoped lang="scss">

</style>
