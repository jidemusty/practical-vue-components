<template>
  <div>
    {{ form }}
    <AppTextarea name="bio" v-model="form.bio" />
  </div>
</template>

<script>
import AppInput from '@/components/AppInput'
import AppLabel from '@/components/AppLabel'
import AppButton from '@/components/AppButton'
import AppTextarea from '@/components/AppTextarea'

export default {
  name: 'home',
  components: {
    AppButton,
    AppInput,
    AppLabel,
    AppTextarea
  },
  data() {
    return {
      form: {
        bio: ''
      }
    }
  },
}
</script>
