<script>
import VFormElement from './VFormElement.vue'

export default {
  name: 'VFormSection',
  components: {
    VFormElement
  },
  props: {
    content: Object
  }
}
</script>

<template>
  <div class="form__section">
    <h3 v-if="content.title">
      {{ content.title }}
    </h3>

    <VFormElement
      v-for="(element, i) of content.elements"
      :key="i"
      :label="element.label"
      :content="element.content"
    />
  </div>
</template>

<style>

</style>
