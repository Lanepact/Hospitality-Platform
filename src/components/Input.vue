<template>
    <input :v-model="modelName" :type="{typeInput}" required>
</template>

<script>
export default {
  name: 'Input',
  props: {
    typeInput: String,
    modelName: String
  }
}
</script>