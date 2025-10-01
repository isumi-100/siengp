<script setup>
import { ref, watch } from 'vue';
import { useRoute } from 'vue-router';
import logo from '../assets/images/SciTokyo_logo.jpg';

const isNavOpen = ref(false);
const route = useRoute();

const toggleNav = () => {
  isNavOpen.value = !isNavOpen.value;
};

const closeNav = () => {
  isNavOpen.value = false;
};

// Route changes should close the nav
watch(() => route.path, () => {
  closeNav();
});
</script>

<template>
  <div id="navArea" :class="{ open: isNavOpen }">
    <header>
      <div class="header_contents">
        <router-link to="/">
          <img :src="logo" alt="東京科学大学ロゴ" />
        </router-link>
        <p>
          <router-link to="/">
            大岡山学生支援センター<br />未来人材育成支援室（学生活動支援）
          </router-link>
        </p>
      </div>
    </header>

    <nav>
      <div class="inner">
        <ul>
          <li><router-link to="/"><span class="material-symbols-outlined">home</span>ホーム</router-link></li>
        </ul>
        <h5>未来人材育成支援室より</h5>
        <ul>
          <li><router-link to="/news">News一覧</router-link></li>
          <li><router-link to="/bbs">電子掲示板システム</router-link></li>
          <li><a href="https://www.titech.ac.jp/student-support/students/extracurricular/crowdfunding" target="_blank" rel="noopener noreferrer">学生クラウドファンディング（大学公式HP）</a></li>
          <li><a href="https://sss.ssc.titech.ac.jp/" target="_blank" rel="noopener noreferrer">みらい創造チャレンジ（外部サイト）</a></li>
        </ul>
        <h5>学生の活動</h5>
        <ul>
          <li><router-link to="/studentsurvey">学勢調査</router-link></li>
          <li><router-link to="/peer">ピアサポーター (理工学系)</router-link></li>
          <li><router-link to="/vg">VG</router-link></li>
          <li><router-link to="/flap">FLAP</router-link></li>
        </ul>
      </div>
    </nav>

    <div class="toggle_btn" @click="toggleNav">
      <span></span>
      <span></span>
      <span></span>
    </div>

    <div id="mask" @click="closeNav"></div>
  </div>
</template>

<style scoped>
header {
  position: fixed;
  width: 100vw;
  height: 100px;
  top: 0;
  background-color: #fff;
  border-bottom: 2px solid #455b86;
  margin: 10;
  z-index: 5000;
  overflow: hidden;
  display: flex; /* for align-items */
  align-items: center;
}

.material-symbols-outlined {
  font-variation-settings: "FILL" 0, "wght" 400, "GRAD" 0, "opsz" 48;
  vertical-align: middle;
}

.header_contents {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  width: 100%;
}

.header_contents img {
  margin: 0;
  height: 80px;
}

.header_contents p {
  margin: 0 0 0 15px;
  font-size: 1.2rem;
  color: #455b86;
  white-space: nowrap;
  line-height: 1.2;
}

.header_contents a {
  display: flex;
  align-items: center;
  text-decoration: none;
  color: #455b86;
}

/* Navigation Styles from common.css */
nav {
  display: none;
  position: fixed;
  top: 0;
  right: -320px; /* Initially hidden */
  bottom: 0;
  width: 320px;
  background: #ffffff;
  overflow-x: hidden;
  overflow-y: auto;
  -webkit-overflow-scrolling: touch;
  transition: all 0.5s;
  z-index: 9999;
  opacity: 0;
}

.open nav {
  display: block;
  right: 0;
  opacity: 1;
}

nav .inner {
  padding: 25px;
}

nav .inner ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

nav .inner ul li {
  position: relative;
  margin: 0;
  border-bottom: 1px solid #333;
}

nav .inner ul li a {
  display: block;
  color: #333;
  font-size: 14px;
  padding: 1em;
  text-decoration: none;
  transition-duration: 0.2s;
}

nav .inner ul li a:hover {
  background: #e4e4e4;
}

/* Toggle Button Styles from common.css */
.toggle_btn {
  display: block;
  position: fixed;
  top: 30px;
  right: 30px;
  width: 30px;
  height: 30px;
  transition: all 0.5s;
  cursor: pointer;
  z-index: 10001;
}

.open .toggle_btn {
  right: 350px;
}

.toggle_btn span {
  display: block;
  position: absolute;
  right: 0;
  width: 30px;
  height: 2px;
  background-color: #333;
  border-radius: 4px;
  transition: all 0.5s;
}

.toggle_btn span:nth-child(1) {
  top: 4px;
}

.toggle_btn span:nth-child(2) {
  top: 14px;
}

.toggle_btn span:nth-child(3) {
  bottom: 4px;
}

.open .toggle_btn span {
  background-color: #333;
}

.open .toggle_btn {
  transform: rotate(360deg);
}

.open .toggle_btn span:nth-child(1) {
  transform: translateY(10px) rotate(45deg);
}

.open .toggle_btn span:nth-child(2) {
  opacity: 0;
}

.open .toggle_btn span:nth-child(3) {
  transform: translateY(-10px) rotate(-45deg);
}

/* Mask Styles from common.css */
#mask {
  display: none;
  transition: all 0.5s;
}

.open #mask {
  display: block;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: #000;
  opacity: 0.8;
  z-index: 9998;
  cursor: pointer;
}

@media screen and (max-width: 670px) {
  header {
    height: 60px;
  }

  .header_contents {
    padding-left: 1rem;
    justify-content: flex-start;
  }

  .header_contents img {
    height: 40px;
  }

  .header_contents p {
    font-size: 0.8rem;
    margin-left: 5px;
  }

  nav {
    width: 220px;
  }

  .open .toggle_btn {
    right: 250px;
  }

  .toggle_btn {
    top: 15px;
  }
}
</style>