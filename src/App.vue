<template>
  <div id="app">
    <ColorPicker />
    <Canvas />
  </div>
</template>

<script>
import Canvas from "@/components/Canvas.vue";
import ColorPicker from "@/components/ColorPicker.vue";

export default {
  name: "app",
  components: {
    Canvas,
    ColorPicker
  }
};
</script>

<style></style>
