<template>
  <button :type="{buttonType}" :style="{background: color}">{{text}}</button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    buttonType: String,
    text: String,
    color: String

  }
}
</script>