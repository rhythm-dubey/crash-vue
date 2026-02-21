<template>
<div>
  <p>Original: {{ message }}</p>
  <p>Reversed: {{ reversedMessage }}</p>
  <p>Character count: {{ characterCount }}</p>
  <input v-model="searchQuery" placeholder="Search...">
</div>
</template>

<script>
export default {
data() {
  return {
    message: 'Hello Vue',
    searchQuery: ''
  }
},
computed: {
  reversedMessage() {
    return this.message.split('').reverse().join('')
  },
  characterCount() {
    return this.message.length
  }
},
watch: {
  searchQuery(newValue, oldValue) {
    console.log(`Search changed from ${oldValue} to ${newValue}`)
    // Could trigger API call here
  }
}
}
</script>