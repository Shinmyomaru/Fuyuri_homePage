<template>
  <div class="homepage">
    <div class="image-container">
      <img 
        src="/src/assets/image.jpg" 
        alt="Fuyuri" 
        class="fade-in-image"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  background-color: #f0f0f0;
}

.homepage {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  padding: 20px;
}

.image-container {
  max-width: 100%;
  max-height: 100vh;
  overflow: hidden;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
  border-radius: 8px;
}

.fade-in-image {
  width: 100%;
  height: auto;
  opacity: 0;
  animation: fadeIn 2s ease-in forwards;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>