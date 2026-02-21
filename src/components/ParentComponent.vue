<template>
<div>
  <ChildComponent 
    title="Hello from Parent" 
    content="This is passed via props"
  />
</div>
</template>

<script>
import ChildComponent from './ChildComponent.vue'

export default {
  components: {
    ChildComponent
  }
}
</script>