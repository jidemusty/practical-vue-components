<template>
  <div>
    <AppButton :to="{ name: 'signin' }" theme="primary" size="normal" />
    <AppButton theme="danger" size="large" />
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
