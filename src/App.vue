<template>
  <div class="home-container" @click="handleImageClick">
    <div class="image-wrapper" :class="{ 'fade-in': isFadedIn }">
      <img 
        src="./assets/homepage/homepage.png" 
        alt="Home Image" 
        class="home-image"
      >
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      isFadedIn: false
    }
  },
  mounted() {
    // 延迟执行渐变效果
    setTimeout(() => {
      this.isFadedIn = true
    }, 100)
  },
  methods: {
    handleImageClick() {
      // 图片点击事件，未来可以在这里添加跳转逻辑
      console.log('Image clicked, ready for navigation')
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.home-container {
  width: 100vw;
  height: 100vh;
  background-color: white;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}

.image-wrapper {
  opacity: 0;
  transition: opacity 2s ease-in;
}

.image-wrapper.fade-in {
  opacity: 1;
}

.home-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>