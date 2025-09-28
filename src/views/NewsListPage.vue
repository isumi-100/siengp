<script setup>
import { newsItems } from '../data/news.js';
</script>

<template>
  <div class="main">
    <div class="contents">
      <div class="txt full-width">
        <h3 style="color: #e97142">News一覧</h3>
      </div>
    </div>

    <div v-for="(item, index) in newsItems" :key="index" class="content">
      <h3 class="title">
        <span v-if="item.category">[{{ item.category }}] </span>{{ item.title }}
      </h3>
      <p>
        {{ item.date }}
        <br />
        <span v-html="item.content"></span>
      </p>
      <router-link v-if="item.link && !item.isExternal" :to="item.link" class="more_btn">
        {{ item.linkText }}
      </router-link>
      <a v-if="item.link && item.isExternal" :href="item.link" class="more_btn" target="_blank" rel="noopener noreferrer">
        {{ item.linkText }}
      </a>
    </div>
  </div>
</template>

<style scoped>
.txt.full-width {
  width: 100%;
}

.content {
  margin-bottom: 2rem;
  padding-bottom: 1rem;
  border-bottom: 1px solid #eee;
}
.title {
  border-bottom: 0.5px solid #455b86;
  font-size: 1.2rem;
}
.more_btn {
  transform: translate(-100%, 0);
  display: inline-block;
  text-align: right;
  border-radius: 10px;
  color: #455b86;
  padding: 12px 25px;
  margin-left: 100%;
  margin-top: 10px;
  white-space: nowrap;
}
.more_btn:hover {
  color: #e97142;
  border: 1px solid #e97142;
  font-weight: bold;
  border-radius: 10px;
}

</style>