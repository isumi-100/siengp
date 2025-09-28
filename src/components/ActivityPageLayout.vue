<template>
  <div class="main sub">
    <slot name="slideshow"></slot>

    <div class="contents">
      <div class="txt" :class="{ 'full-width': !logo }">
        <h3>{{ title }}</h3>
        <p v-html="description"></p>
      </div>
      <img v-if="logo" :src="logo" alt="" />
    </div>

    <div class="introduction">
      <slot name="details"></slot>
    </div>
  </div>
</template>

<script setup>
defineProps({
  title: String,
  description: String,
  logo: String,
});
</script>

<style scoped>
.txt.full-width {
  width: 100%;
}
</style>