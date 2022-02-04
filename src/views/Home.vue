<template>
  <div class="home">
    <VForm
      icon="logo.png"
      heading="Test"
      :inputs="[
        {
          label: 'Email',
          type: 'email'
        },
        {
          label: 'Password',
          type: 'password'
        },
        {
          type: 'select',
          options: [
            {
              value: 'a',
              content: 'Option A'
            },
            {
              value: 'b',
              content: 'Option B'
            }
          ]
        }
      ]"
    />
  </div>
</template>

<script>
import VForm from '@/components/VForm.vue'

export default {
  name: 'Home',
  components: {
    VForm
  }
}
</script>
