<template>
<div>
  <!-- Text interpolation -->
  <p>
      {{ message }}
  </p>

  
  <!-- Raw HTML -->
  <p v-html="rawHtml"></p>

  <!-- JavaScript expressions -->
  <p>{{ count + 1 }}</p>
  <p>{{ message.split('').reverse().join('') }}</p>
</div>
</template>

<script>
export default {
  data() {
    return {
      message: 'Hello World',
      rawHtml: '<strong>Bold text</strong>',
      count: 5
    }
  }
}
</script>

<style>
</style>