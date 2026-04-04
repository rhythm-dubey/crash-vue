<template>
  <div>
    <button class="btn btn-primary" @click="openModal">
      Open Modal
    </button>

    <div class="modal fade" id="myModal" ref="modalRef" tabindex="-1">
      <div class="modal-dialog">
        <div class="modal-content">
          
          <div class="modal-header">
            <h5 class="modal-title">Hello</h5>
            <button class="btn-close" data-bs-dismiss="modal"></button>
          </div>

          <div class="modal-body">
            <p>This is modal</p>
          </div>

        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import { Modal } from 'bootstrap'

const modalRef = ref(null)
let modalInstance = null

onMounted(() => {
  if (modalRef.value) {
    modalInstance = new Modal(modalRef.value)
  }
})

const openModal = () => {
  if (modalInstance) {
    modalInstance.show()
  }
}
</script>