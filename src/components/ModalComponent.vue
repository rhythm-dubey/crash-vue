<template>
  <div>
    <!-- Button -->
    <button class="btn btn-primary" @click="openModal('Hello', 'This is dynamic content')">
      Open Modal
    </button>

    <!-- Modal -->
    <div class="modal fade show" tabindex="-1" style="display: block;" v-if="isOpen">
      <div class="modal-dialog">
        <div class="modal-content">
          
          <div class="modal-header">
            <h5 class="modal-title">{{ modalData.title }}</h5>
            <button class="btn-close" @click="closeModal"></button>
          </div>

          <div class="modal-body">
            <p>{{ modalData.body }}</p>
          </div>

          <div class="modal-footer">
            <button class="btn btn-secondary" @click="closeModal">Close</button>
          </div>

        </div>
      </div>
    </div>

    <!-- Backdrop -->
    <div class="modal-backdrop fade show" v-if="isOpen"></div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const isOpen = ref(false)

const modalData = ref({
  title: '',
  body: ''
})

const openModal = (title, body) => {
  modalData.value = { title, body }
  isOpen.value = true
}

const closeModal = () => {
  isOpen.value = false
}
</script>