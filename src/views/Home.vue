<template>
  <div>
    <AppInput name="first_name" type="password" />
  </div>
</template>

<script>
import AppInput from '@/components/AppInput'
import AppButton from '@/components/AppButton'

export default {
  name: 'home',
  components: {
    AppButton,
    AppInput
  },
  methods: {
    doThis() {
      console.log('yaaay')
    }
  }
}
</script>
