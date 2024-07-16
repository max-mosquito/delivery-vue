<script setup>
  import Header from './components/Header.vue';
  import Footer from './components/Footer.vue';
  import Modal from './components/Modalw.vue';
import { ref } from 'vue';

  const isOpen = ref(false);
</script>

<template>
  <div class="page-wrapper">
    
    <Header @toggleModal="isOpen = !isOpen"></Header>

    <main class="main">
      <router-view></router-view>
    </main>
    
    <Footer></Footer>

    <Modal :isOpen="isOpen" @toggleModal="isOpen = !isOpen"></Modal>
    
  </div>
</template>

<style scoped>

</style>
