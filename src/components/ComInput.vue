<template>
  <div class="transition-all duration-200 justify-center flex items-center">
    <input
      class="form-input rounded-lg bg-gray-100 p-2 border-primary bg-primary-hover border-none text-default placeholder-white"
      :type="'number'"
      :placeholder="placeholder"
      :value="value"
      @input="$emit('update:value', $event.target.value)"
    />
  </div>
</template>

<script>
export default {
  props: {
    placeholder: {
      type: String,
      default: ''
    },
    value: {
      type: [Number]
    }
  }
}
</script>

<style lang="css" scoped></style>
