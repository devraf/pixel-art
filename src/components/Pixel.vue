<template>
  <div
    v-on:click="interactive && changeColor(color)"
    v-bind:class="['pixel', color, current ? 'current' : '']"
  ></div>
</template>

<script>
export default {
  name: "Pixel",
  props: {
    color: String,
    current: Boolean,
    interactive: Boolean
  },
  methods: {
    changeColor: function(color) {
      this.$root.$emit("updatecolor", color);
    }
  }
};
</script>

<style scoped>
.pixel {
  border: 1px solid lightgray;
  width: 25px;
  height: 25px;
  box-sizing: border-box;
}
.pixel.current {
  border: 4px solid yellow;
}
.white {
  background-color: white;
}
.lightblue {
  background-color: rgb(0, 188, 212);
}
.blue {
  background-color: rgb(3, 169, 244);
}
.darkblue {
  background-color: rgb(33, 150, 243);
}
</style>
