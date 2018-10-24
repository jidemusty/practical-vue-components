<template>
    <input
        :type="type"
        :name="name"
        :id="name"
        class=""
    />
</template>

<script>
export default {
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
    }
}
</script>
