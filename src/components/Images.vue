<template>
  <img :src="source">
</template>

<script>
export default {

  name: 'Images',
  props: ['source'],
  data() {
    return {
      imagePath: this.source
    } 
  }
}
</script>