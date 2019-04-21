<template>
  <div class="canvas">
    <Pixel v-for="n in 30 * 30" :key="n" color="blue" />
  </div>
</template>

<script>
import Pixel from "@/components/Pixel.vue";

export default {
  name: "Canvas",
  components: {
    Pixel
  }
};
</script>

<style>
.canvas {
  display: flex;
  flex-wrap: wrap;
  max-width: 900px;
}
</style>
