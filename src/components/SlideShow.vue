<template>
  <div class="auto-slideshow">
    <div class="slideshow-inner">
      <div class="slide-container" :style="slideContainerStyle">
        <figure v-for="(slide, index) in slides" :key="index">
          <img :src="slide.imgSrc" :alt="slide.altText" />
          <figcaption>{{ slide.caption }}</figcaption>
        </figure>
      </div>
      <div class="indicators">
        <span
          v-for="(_, index) in slides"
          :key="index"
          class="dot"
          :class="{ active: currentSlide === index }"
        ></span>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed, onMounted, onUnmounted } from 'vue';

const props = defineProps({
  slides: {
    type: Array,
    required: true,
    default: () => []
  },
});

const currentSlide = ref(0);
let timer = null;

const slideContainerStyle = computed(() => {
  return {
    transform: `translateX(-${currentSlide.value * 100}%)`,
  };
});

onMounted(() => {
  timer = setInterval(() => {
    currentSlide.value = (currentSlide.value + 1) % props.slides.length;
  }, 5000);
});

onUnmounted(() => {
  clearInterval(timer);
});
</script>

<style scoped>
.auto-slideshow {
  width: 50vw;
  height: 500px;
  margin: 20px auto 20px;
  overflow: hidden;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  position: relative;
}

.slideshow-inner {
  width: 100%;
  height: 93%;
  top: 10px;
  position: relative;
}
.slide-container {
  display: flex;
  height: 100%;
  transition: transform 1.2s ease-in-out;
}

.slide-container figure {
  width: 100%;
  height: 100%;
  flex-shrink: 0;
  margin: 0;
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.slide-container img {
  width: 100%;
  height: 100%;
  object-fit: contain; /* 画像全体が表示されるように変更 */
  display: block;
}

.slide-container figcaption {
  position: relative;
  width: 100%;
  color: #181818;
  padding: 10px;
  text-align: center;
  font-size: 0.9rem;
  box-sizing: border-box;
  z-index: 1;
}

.indicators {
  position: absolute;
  bottom: -25px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  gap: 8px;
}

.dot {
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background-color: rgba(0, 0, 0, 0.2);
  transition: background-color 0.3s;
}

.dot.active {
  background-color: #455b86;
}
@media screen and (max-width: 1072px) {
  .auto-slideshow {
    width: 80%;
    max-height: 350px;
    margin: 3px auto;
  }
  .slideshow-inner {
    height: 90%;
  }
}
@media screen and (max-width: 680px) {
  .auto-slideshow {
    width: 80%;
    max-height: 300px;
    margin: 6px auto;
  }
  .slideshow-inner {
    height: 90%;
  }
}
</style>