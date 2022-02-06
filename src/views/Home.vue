<script>
import VForm from '@/components/VForm.vue'

export default {
  name: 'Home',
  components: {
    VForm
  }
}
</script>

<template>
  <VForm
    :onSubmit="() => {}"
    :prevent="true"
    :sections="[
      {
        title: 'shipping information',
        elements: [
          {
            label: 'name',
            content: [
              {
                holder: 'first name'
              },
              {
                holder: 'last name'
              }
            ]
          },
          {
            label: 'billing address',
            content: [
              {
                holder: 'street address'
              },
              {
                type: 'number',
                holder: 'house number'
              }
            ]
          }
        ]
      },
      {
        title: 'billing information',
        elements: []
      },
      {
        title: 'receipt',
        elements: []
      }
    ]"
  />
</template>
