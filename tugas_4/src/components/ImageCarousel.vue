<template>
  <div>
    <h2>Image Carousel</h2>
    <div>
      <img :src="images[currentImage]" :alt="'Image ' + (currentImage + 1)" style="max-width: 100%;" />
    </div>
    <button @click="prevImage">Previous</button>
    <button @click="nextImage">Next</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentImage: 0,
      images: [
        'https://via.placeholder.com/300x200?text=Image+1',
        'https://via.placeholder.com/300x200?text=Image+2',
        'https://via.placeholder.com/300x200?text=Image+3'
      ]
    };
  },
  methods: {
    prevImage() {
      this.currentImage = (this.currentImage + this.images.length - 1) % this.images.length;
    },
    nextImage() {
      this.currentImage = (this.currentImage + 1) % this.images.length;
    }
  }
};
</script>
