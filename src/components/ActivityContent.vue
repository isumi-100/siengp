<template>
  <div class="txt">
    <h3>{{ title }}</h3>
    <p v-html="description"></p>
  </div>
  <img :src="logo" alt="" />
</template>

<script setup>
defineProps({
  title: String,
  description: String,
  logo: String,
});
</script>