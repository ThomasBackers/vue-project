<script>
import VFormContent from './VFormContent.vue'

export default {
  name: 'VFormElement',
  components: {
    VFormContent
  },
  props: {
    label: String,
    content: Array
  }
}
</script>

<template>
  <label v-if="label">
    {{ label }}
    <VFormContent
      v-for="(object, i) of content"
      :key="i"
      :object="object"
    />
  </label>

  <div v-else>
    <VFormContent
      v-for="(object, i) of content"
      :key="i"
      :object="object"
    />
  </div>
</template>

<style>

</style>
