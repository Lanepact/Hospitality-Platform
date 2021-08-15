<template>
    <input :type="{typeInput}" required>
</template>

<script>
export default {
  name: 'Input',
  props: {
    typeInput: String,
  }
}
</script>