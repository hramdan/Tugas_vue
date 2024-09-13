<template>
  <div id="app">
    <ClickCounter />
    <ColorBox />
    <ImageCarousel />
  </div>
</template>

<script>
import ClickCounter from './components/ClickCounter.vue';
import ColorBox from './components/ColorBox.vue';
import ImageCarousel from './components/ImageCarousel.vue';

export default {
  components: {
    ClickCounter,
    ColorBox,
    ImageCarousel
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>