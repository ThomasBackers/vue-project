<script>
import VFormSection from './VFormSection.vue'

export default {
  name: 'VForm',
  components: {
    VFormSection
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
    onSubmit: {
      type: Function,
      default: () => {}
    },
    prevent: {
      type: Boolean,
      default: false
    },
    sections: {
      type: Array,
      required: true
    }
  }
}
</script>

<template>
  <form
    v-if="!prevent"
    class="form"
    :action="action"
    :method="method"
    @submit="onSubmit"
  >
    <VFormSection
      v-for="(section, i) of sections"
      :key="i"
      :content="section"
    />
  </form>

  <form
    v-else
    class="form"
    :action="action"
    :method="method"
    @submit.prevent="onSubmit"
  >
    <VFormSection
      v-for="(section, i) of sections"
      :key="i"
      :content="section"
    />
  </form>
</template>

<style>

</style>
