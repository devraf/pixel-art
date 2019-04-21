<template>
  <div>
    <Pixel
      interactive
      color="white"
      :current="color == 'white' ? true : false"
    />
    <Pixel
      interactive
      color="lightblue"
      :current="color == 'lightblue' ? true : false"
    />
    <Pixel interactive color="blue" :current="color == 'blue' ? true : false" />
    <Pixel
      interactive
      color="darkblue"
      :current="color == 'darkblue' ? true : false"
    />
    <!-- <p>{{ color }}</p>
    <p>{{ myNewProp }}</p>-->
  </div>
</template>

<script>
import Pixel from "@/components/Pixel.vue";

export default {
  name: "ColorPicker",
  props: {
    color: String,
    myNewProp: String
  },
  components: {
    Pixel
  }
};
</script>

<style></style>
