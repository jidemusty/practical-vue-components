<template>
  <div>
    <AppButton :to="{ name: 'signin' }" theme="primary" size="normal" />
    <AppButton theme="danger" size="large" disabled @click.prevent="doThis" />
  </div>
</template>

<script>
import AppButton from '@/components/AppButton'

export default {
  name: 'home',
  components: {
    AppButton
  },
  methods: {
    doThis() {
      console.log('yaaay')
    }
  }
}
</script>
