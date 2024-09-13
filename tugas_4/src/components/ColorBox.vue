<template>
  <div class="color-box-container">
    <h2>Box Color Changer</h2>
    <div :style="{ backgroundColor: boxColor }" class="color-box"></div>
    <button @click="changeColor">Change Color</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      boxColor: 'blue'
    };
  },
  methods: {
    changeColor() {
      const colors = ['blue', 'red', 'green', 'yellow', 'purple'];
      this.boxColor = colors[Math.floor(Math.random() * colors.length)];
    }
  }
};
</script>

<style scoped>
.color-box-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 300px; /* Adjust based on your need */
}

.color-box {
  width: 100px;
  height: 100px;
  margin-bottom: 10px;
}
</style>
