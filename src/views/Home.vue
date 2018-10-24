<template>
  <div>
    <AppLabel forInput="first_name">First name</AppLabel>
    <AppInput name="first_name" type="email" placeholder="Enter your email" />
  </div>
</template>

<script>
import AppInput from '@/components/AppInput'
import AppLabel from '@/components/AppLabel'
import AppButton from '@/components/AppButton'

export default {
  name: 'home',
  components: {
    AppButton,
    AppInput,
    AppLabel
  },
  data() {
    return {
      form: {
        email: 'ejooooo'
      }
    }
  },
  methods: {
    doThis() {
      console.log('yaaay')
    }
  }
}
</script>
