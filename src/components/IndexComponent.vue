<template>
	<div :style="{position: modal ? 'fixed' : ''}">
    <p>test</p>
    <!-- <button @click="openModal">open modal</button> -->
    <NavButton @click="modal = !modal" class="btn-nav" :opened="isOpen" :disabled="isDisabled" />
    <Modal :show="modal" @toggle-status="isOpen = !isOpen" @d-status="(val) => isDisabled = val" />
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusamus doloribus libero iste corrupti dolore, distinctio et. Sunt nesciunt, vero earum maiores laudantium et officiis expedita, architecto quae laborum tenetur ut.</p>
  </div>
</template>

<script>
import Modal from './Modal.vue'
import NavButton from './NavButton.vue'

export default {
  components: {
    Modal,
    NavButton
  },
  data() {
    return {
      modal: false,
      isOpen: false,
      isDisabled: false,
    }
  },
  methods: {
    openModal() {
      this.modal = true
    }
  },
}
</script>

<style scoped>
.btn-nav {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 20;
}
</style>
