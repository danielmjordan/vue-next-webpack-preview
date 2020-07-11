<template>
  <button @click="toggleModalState">Open modal</button>
  <Modal v-if="modalOpen" @close="toggleModalState">
    <p>Hello, I'm a modal window.</p>
  </Modal>
</template>

<script>
import Modal from './Modal.vue';
import { ref } from 'vue';
export default {
  setup() {
    const modalOpen = ref(false);
    const toggleModalState = () => {
      modalOpen.value = !modalOpen.value;
    };
    return {
      modalOpen,
      toggleModalState,
    };
  },
  components: {
    Modal,
  },
};
</script>
