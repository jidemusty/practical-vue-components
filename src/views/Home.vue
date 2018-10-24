<template>
  <div>
    <AppModal />
  </div>
</template>

<script>
import AppInput from '@/components/AppInput'
import AppLabel from '@/components/AppLabel'
import AppButton from '@/components/AppButton'
import AppTextarea from '@/components/AppTextarea'
import AppModal from '@/components/AppModal'

export default {
  name: 'home',
  components: {
    AppButton,
    AppInput,
    AppLabel,
    AppTextarea,
    AppModal
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
