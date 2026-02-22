<template>
  <button @click="sendData">Send to Parent</button>
</template>

<script>
export default {
  emits: ['data-sent'],
  methods: {
    sendData() {
      this.$emit('data-sent', 'Data from child')
    }
  }
}
</script>