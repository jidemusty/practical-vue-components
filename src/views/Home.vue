<template>
  <div>
    {{ form }}
    <AppInput name="first_name" type="email" v-model="form.email" />
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
  data() {
    return {
      form: {
        email: ''
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
