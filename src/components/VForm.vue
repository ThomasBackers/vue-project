<template>
  <form action="" method="post">
    <img src="" alt="">

    <h3 v-if="heading">{{ heading }}</h3>

    <VInput>
  </form>
</template>

<script>
import VInput from '@/components/VInput.vue'

export default {
  name: 'VForm',
  components: {
    VInput
  },
  props: ['heading']
}
</script>

<style scoped lang="scss">

</style>
