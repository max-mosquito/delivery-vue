<script setup>
  import Header from './components/Header.vue';
  import Footer from './components/Footer.vue';
  import Modal from './components/Modalw.vue';
import { ref } from 'vue';

  const isOpen = ref(false);
</script>

<template>
  <div class="page-wrapper">
    
    <Header @toffleModal="isOpen = !isOpen"></Header>

    <main class="main">
      <router-view></router-view>
    </main>
    
    <Footer></Footer>

    <Modal :isOpen="isOpen" @toffleModal="isOpen = !isOpen"></Modal>
    
  </div>
</template>

<style scoped>

</style>
