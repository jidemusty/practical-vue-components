<template>
    <div>
        <input
            :type="inputType"
            :name="name"
            :id="name"
            class="block mb-2 p-3 shadow-outline w-full"
        />

        <a href="#" v-if="type == 'password'" @click.prevent="passwordRevealed = !passwordRevealed">
            {{ passwordRevealed ? 'Hide' : 'Reveal' }} Password
        </a>
    </div>
</template>

<script>
export default {
    data () {
        return {
            passwordRevealed: false
        }
    },
    props: {
        type: {
            required: false,
            type: String,
            default: "text"
        },
        name: {
            required: true,
            type: String,
        }
    },
    computed: {
        inputType () {
            return this.passwordRevealed ? 'text' : this.type
        }
    },
    methods: {
        toggleVisibility () {
            this.inputType = this.inputType === 'password' ? 'text' : 'password'
        }
    }
}
</script>
