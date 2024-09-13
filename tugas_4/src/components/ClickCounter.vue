<template>
  <div>
    <h2>Click Counter</h2>
    <p>You have clicked the button {{ count }} times.</p>
    <button @click="count++">Click me</button>
    <button @click="resetCount" style="margin-left: 10px;">Reset</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    };
  },
  methods: {
    resetCount() {
      this.count = 0;
    }
  }
};
</script>