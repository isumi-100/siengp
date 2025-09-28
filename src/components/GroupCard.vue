<script setup>
defineProps({
  to: String,
  imageSrc: String,
  altText: String,
});
</script>

<template>
  <router-link :to="to" class="group">
    <img :src="imageSrc" :alt="altText" />
    <span class="group_btn"><slot></slot> ></span>
  </router-link>
</template>