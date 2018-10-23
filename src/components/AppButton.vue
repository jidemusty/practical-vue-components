<template>
    <router-link 
        class="px-5 py-2 border-none no-underline rounded text-white"
        :to=to
        :class="{
            'bg-blue': primary,
            'bg-red': danger
        }"
    >
        Sign In
    </router-link>
</template>

<script>
export default {
    props: {
        primary: {
            required: false,
            type: Boolean,
            default: true
        },
        danger: {
            required: false,
            type: Boolean,
            default: false
        },
        to: {
            required: false,
            type: Object,
            default () {
                return {
                    name: 'home'
                }
            }
        }
    }
}
</script>
