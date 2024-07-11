<script setup>
import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
  <div class="raiz">
    <HelloWorld />
  </div>
  <div class="prueba">Hola Prueba</div>
</template>
<style scoped>
.raiz {
  position: fixed;
  width: 100vw;
  height: 100vh;
  top: 0;
  left: 0;
}

.prueba {
  z-index: 1;
  color: aliceblue;
}
</style>
