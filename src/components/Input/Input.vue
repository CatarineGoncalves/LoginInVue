<template>
  <div class="input-container">
    <input
      :type="inputType"
      :id="id"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
      placeholder=" "
      required
    />
    <label :for="id">{{ label }}</label>
  </div>
</template>

<script>
export default {
  name: 'Input',
  props: {
    modelValue: String,
    inputType: String,
    id: String,
    label: String
  }
}
</script>

<style scoped>
@import './Input.css';
</style>
