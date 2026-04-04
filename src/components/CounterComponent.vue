<template>
  <h1>
    {{ count }}
  </h1>
  <br />
  <button @click='increment'
    class='btn btn-primary'
    >
    +</button>
  <button @click='decrement'
    class='btn btn-danger'
    >-</button>

  <ModalComponent />
</template>



<script>
import ModalComponent from './ModalComponent.vue';

export default {
  data() {
    return {
      count: 0
    }
  },
  components: {
    ModalComponent
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
