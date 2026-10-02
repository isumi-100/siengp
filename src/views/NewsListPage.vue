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

      <!-- 添付ファイル：左寄せリスト -->
      <ul v-if="item.files?.length" class="file-list">
        <li
            v-for="(file, fileIndex) in item.files"
            :key="fileIndex"
        >
          <a
              :href="file.url"
              target="_blank"
              rel="noopener noreferrer"
          >
            {{ file.text }}
          </a>
        </li>
      </ul>

      <!-- 従来リンク：右寄せ -->
      <div class="links">
        <!-- 内部ページ -->
        <router-link
            v-if="item.link && !item.isExternal && !item.link.endsWith('.pdf')"
            :to="item.link"
            class="more_btn"
        >
          {{ item.linkText }}
        </router-link>

        <!-- 外部リンク・PDF -->
        <a
            v-if="item.link && (item.isExternal || item.link.endsWith('.pdf'))"
            :href="item.link"
            class="more_btn"
            target="_blank"
            rel="noopener noreferrer"
        >
          {{ item.linkText }}
        </a>
      </div>
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

/* 添付ファイル */
.file-list {
  margin: 0.8rem 0;
  padding-left: 1.5rem;
  text-align: left;
}

.file-list li {
  margin-bottom: 0.3rem;
}

.file-list a {
  color: #455b86;
  text-decoration: underline;
}

.file-list a:hover {
  color: #e97142;
}

/* 従来の「詳しく見る」 */
.links {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-end;
  gap: 0.5rem;
  margin-top: 10px;
}

.more_btn {
  display: inline-block;
  text-align: center;
  border-radius: 10px;
  color: #455b86;
  padding: 12px 25px;
  white-space: nowrap;
}

.more_btn:hover {
  color: #e97142;
  border: 1px solid #e97142;
  font-weight: bold;
  border-radius: 10px;
}
</style>