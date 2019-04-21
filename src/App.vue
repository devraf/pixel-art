<template>
  <div id="app">
    <ColorPicker v-bind:color="color" v-bind:myNewProp="dataFromParent" />
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
  },
  data() {
    return {
      color: "my new color",
      dataFromParent: "This is data passed from parent to component via a prop"
    };
  },
  mounted() {
    this.$root.$on("updatecolor", color => {
      this.color = color;
    });
  }
};
</script>

<style>
* {
  margin: 0;
}
#app {
  background-color: #333;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
</style>
