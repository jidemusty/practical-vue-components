<template>
    <textarea
        v-bind="$attrs"
        :name="name"
        :id="name"
        :value="value"
        class="block mb-2 mt-2 p-3 shadow-outline w-full"
        @input="$emit('input', $event.target.value)"
    ></textarea>
</template>

<script>
export default {
  props: {
    value: {
      required: false,
      type: String,
      default: ""
    },
    name: {
      required: true,
      type: String
    }
  }
};
</script>
