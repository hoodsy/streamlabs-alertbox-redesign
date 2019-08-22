<template>
  <div class="theme-slider">
    <div class="theme-slider-button">
      <i class="fas fa-chevron-right fa-lg"></i>
    </div>
    <div class="theme-items">
      <img
        class="theme-item"
        v-for="image in images"
        :src="image.url"
        :alt="image.alt"
        :key="image.id"
      />
    </div>
  </div>
</template>

<script>
import { mockThemeImages } from "../data/mock";

export default {
  name: "AlertBoxThemeSlider",
  props: {
    images: {
      type: Array,
      default: () => mockThemeImages
    }
  }
};
</script>

<style scoped>
.theme-slider {
  position: relative;
  background: #2e383f;
  width: 100%;
  max-width: calc(
    1600px - 240px
  ); /* dashboard-body width - dashboard-sidenav width */
  height: 256px;
  padding: 4px;
  margin-bottom: 64px;
  border-radius: 4px;
}

.theme-items {
  display: flex;
  flex-wrap: nowrap;
  overflow: hidden;
}

.theme-item {
  height: 256px;
  margin-right: 4px;
}

.theme-slider-button {
  box-sizing: border-box;
  position: absolute;
  right: 4px;
  top: 4px;
  height: calc(100% - 8px);
  padding: 32px;
  background: #0e1820;
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0.7;
  transition: opacity 0.5s ease-in;
}
.theme-slider-button:hover {
  opacity: 1;
  cursor: pointer;
}
</style>
