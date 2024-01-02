<script setup>
import Modal from './tModal.vue'
import { ref } from 'vue'

const showModal = ref(false)
</script>

<template>
  <button id="show-modal" @click="showModal = true"> 모달 보여주기 </button> 

  <Teleport to="body">
    <modal :show="showModal" @close="showModal = false">
     <template #header>
        <h3> 커스텀 header</h3>
      </template>

      <template #body>
        커스텀 바디
      </template>
    </modal>
  </Teleport>
</template>