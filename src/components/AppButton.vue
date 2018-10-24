<template>
    <router-link 
        class="border-none no-underline rounded text-white"
        :to=to
        :class="[
            themes[theme],
            sizes[size]
        ]"
    >
        Sign In
    </router-link>
</template>

<script>
export default {
    data() {
        return {
            themes: {
                primary: 'bg-blue',
                danger: 'bg-red'
            },
            sizes: {
                normal: 'px-4 py-2',
                large: 'px-6 py-4'
            }
        }
    },
    props: {
        theme: {
            required: false,
            type: String,
            default: 'primary'
        },
        size: {
            required: false,
            type: String,
            default: 'normal'
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
