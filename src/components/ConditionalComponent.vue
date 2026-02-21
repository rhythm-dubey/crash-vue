<template>
  <div>
    <!-- Conditional rendering -->
    <p v-if="isVisible">Visible</p>
    <p v-else>Hidden</p>

    <!-- Loop through arrays -->
    <ul>
        <li v-for="(item, index) in items" :key="index">
        {{ index }}: {{ item }}
        </li>
    </ul>

    <!-- Event handling -->
    <button v-on:click="handleClick">Click me</button>
    <!-- Shorthand -->
    <button @click="handleClick">Click me</button>

    <!-- Two-way binding -->
    <input v-model="inputText" />
    <p>You typed: {{ inputText }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isVisible: true,
      items: ['Apple', 'Banana', 'Orange'],
      inputText: ''
    }
  },
  methods: {
    handleClick() {
      alert('Button clicked!')
    }
  }
}
</script>

<style>
</style>