<template>
    <div>
        <input
            v-bind="$attrs"
            :type="inputType"
            :name="name"
            :id="name"
            :value="value"
            class="block mb-2 mt-2 p-3 shadow-outline w-full"
            @input="$emit('input', $event.target.value)"
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
        value: {
            required: false,
            type: String,
            default: ""
        },
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
    },
}
</script>
