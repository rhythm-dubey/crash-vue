<template>
  <h1>
    {{ count }}
  </h1>
  <br />
  <button @click='increment'>+</button>
  <button @click='decrement'>-</button>
</template>



<script>
export default {
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increment() {
      this.count++
    },
    decrement() {
      this.count--
    }
  }
}
</script>
