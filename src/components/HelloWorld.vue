<script setup>
import { shallowRef } from "vue";
import { TresCanvas, useRenderLoop } from "@tresjs/core";
import { OrbitControls, Stars } from "@tresjs/cientos";

const yRotation = shallowRef(0);
useRenderLoop().onLoop(({ delta }) => {
  yRotation.value += 0.02 * delta;
});
</script>

<template>
  <TresCanvas class="color">
    <TresPerspectiveCamera />
    <Stars
      :rotation="[0, yRotation, 0]"
      :radius="50"
      :depth="50"
      :count="5000"
      :size="0.3"
      :size-attenuation="true"
    />
  </TresCanvas>
</template>
<style scoped>
.color {
  background-color: #222;
}
</style>
