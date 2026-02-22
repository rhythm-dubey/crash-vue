<template>
<EventChildComponent @data-sent="handleChildData" />
</template>

<script>
import EventChildComponent from './EventChildComponent.vue'

export default {
  components: {
    EventChildComponent
  },
  methods: {
      handleChildData(data) {
      console.log('Received:', data)
    }
  }
}
</script>