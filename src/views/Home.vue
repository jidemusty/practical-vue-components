<template>
  <div>
    <AppButton :to="{ name: 'signin' }" />
    <AppButton danger />
  </div>
</template>

<script>
import AppButton from '@/components/AppButton'

export default {
  name: 'home',
  components: {
    AppButton
  }
}
</script>
