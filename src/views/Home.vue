<template>
  <div>
    <app-sign-in-modal />
    <a href="#" @click.prevent="$modal.show('signin')">Open Modal</a>
  </div>
</template>

<script>
import AppInput from '@/components/AppInput'
import AppLabel from '@/components/AppLabel'
import AppButton from '@/components/AppButton'
import AppTextarea from '@/components/AppTextarea'
import AppModal from '@/components/AppModal'
import AppSignInModal from '@/components/modals/AppSignInModal'

export default {
  name: 'home',
  components: {
    AppButton,
    AppInput,
    AppLabel,
    AppTextarea,
    AppModal,
    AppSignInModal
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
