<template>
  <Navbar />
  <Mainvue />
  <div class="bg-orange-200 text-center font-bold">
    <p :class="show">Esto es un texto condicional en App.vue</p>
  </div>
  
  <Footervue />
</template>

<script setup>
import Navbar from './components/Navbar.vue';
import Mainvue from './components/MainVue.vue';
import Footervue from './components/FooterVue.vue';
import { ref } from 'vue';

const show = ref('show');

</script>

<style scoped>
.show{
  display: block;
}

.hidden{
  display: none;
}

</style>

