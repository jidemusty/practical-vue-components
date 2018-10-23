<template>
    <router-link 
        class="bg-blue px-5 py-2 border-none no-underline rounded text-white"
        :to=to
    >
        Sign In
    </router-link>
</template>

<script>
export default {
    props: {
        to: {
            required: false,
            type: Object,
            default () {
                return {
                    name: 'signin'
                }
            }
        }
    }
}
</script>
