<template>
    <router-link
        @click.native="clicked"
        class="border-none no-underline rounded text-white"
        :disabled="disabled"
        :to=to
        :class="[
            themes[theme],
            sizes[size], {
                'opacity-50 cursor-not-allowed': disabled
            }
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
        disabled: {
            required: false,
            type: Boolean,
            default: false
        },
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
    },
    methods: {
        clicked(e) {
            if (this.disabled) {
                return
            }

            this.$emit('click', e)
        }
    }
}
</script>
