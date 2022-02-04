<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <VForm
      action=""
      method="post"
      icon="logo.png"
      heading="Test"
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
