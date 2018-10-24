<template>
  <div>
    <AppButton :to="{ name: 'signin' }" theme="primary" size="normal">
      Create an account &rarr;
    </AppButton>
    <AppButton theme="danger" size="large" disabled @click.prevent="doThis">
      Upvote
    </AppButton>
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
