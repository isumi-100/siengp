<script setup>
import { newsItems } from '../data/news.js';
import GroupCard from '../components/GroupCard.vue';
const latestNews = newsItems.slice(0, 3);

import studentSurveyLogo from '../assets/images/studentsurvey/logo.png';
import vgLogo from '../assets/images/vg/logo.jpg';
import peerLogo from '../assets/images/peer/psm.png';
import flapLogo from '../assets/images/flap/logo.jpg';
</script>

<template>
  <div class="fade-in">
    <div class="main_top">
      <div class="tabs">
        <a href="#activities">学生の活動</a>
        <router-link to="/bbs"
          >電子掲示板システム<br />（デジタルサイネージ）</router-link
        >
        <a
          href="https://www.titech.ac.jp/student-support/students/extracurricular/crowdfunding"
          >学生クラウドファンディング<br />
          （大学公式HP）
        </a>
        <a href="https://sss.ssc.titech.ac.jp/"
          >みらい創造チャレンジ<br />
          （外部サイト）</a
        >
      </div>
      <div class="news">
        <h3 class="title">○ 新着News</h3>
        <p v-for="item in latestNews" :key="item.title">
          <component
            :is="item.link && !item.isExternal ? 'router-link' : 'a'"
            :to="item.link && !item.isExternal ? (item.link || '/news') : undefined"
            :href="item.link && item.isExternal ? item.link : (!item.link ? '/news' : undefined)"
            :target="item.isExternal ? '_blank' : undefined"
            :rel="item.isExternal ? 'noopener noreferrer' : undefined"
          >
            ＊ <span v-if="item.category">[{{ item.category }}] </span>
            {{ item.title }}
            <span>({{ item.date }})</span>
          </component>
        </p>
        <router-link to="/news" class="more_btn"> News一覧はこちら -> </router-link>
      </div>
      <div class="activities">
        <h3 class="title" id="activities">○ 学生の活動</h3>
        <p>
          未来人材育成支援室が現在支援している学生の活動は、以下の4活動です。
          <br />各活動の詳細は 下記からご確認ください。
        </p>
        <div class="groups">
          <GroupCard to="/studentsurvey" :imageSrc="studentSurveyLogo" altText="学勢調査">
            学勢調査
          </GroupCard>
          <GroupCard to="/vg" :imageSrc="vgLogo" altText="学生ボランティアグループ（VG）">
            学生ボランティア<br />グループ（VG）
          </GroupCard>
          <GroupCard to="/peer" :imageSrc="peerLogo" altText="理工学系ピアサポーター">
            理工学系<br />ピアサポーター
          </GroupCard>
          <GroupCard to="/flap" :imageSrc="flapLogo" altText="留学促進団体FLAP">
            留学促進団体FLAP
          </GroupCard>
        </div>
      </div>
      <div class="about">
        <h3 class="title">未来人材育成支援室（学生活動支援）について</h3>
        <p>
          大岡山学生支援センター未来人材育成支援室（学生活動支援）では、学生たちの主体的な活動を支援しています。
          <br />学生たちの活動に教職員が協同して関与することで、学生が活動において壁に直面した時のフォローアップや、
          自律を促す指導・助言、活動拠点の提供等をおこなっています。
        </p>
        <router-link to="/member" class="more_btn"
          >学生支援センター自律支援実施委員会<br />委員名簿 ->
        </router-link>
      </div>
      <div class="about">
        <h3 class="title">○ 関連サイト</h3>
        <ul>
          <li><a href="https://www.isct.ac.jp/ja">東京科学大学公式HP</a></li>
          <li>
            <a
              href="https://www.isct.ac.jp/ja/001/about/organizations/student-support-center"
              >東京科学大学 学生支援センター HP</a
            >
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@24,400,0,0");
.main_top {
  width: 60%;
  margin-left: 20%;
  margin-top: 120px;
  animation-name: fade;
  animation-duration: 2s;
}
.tabs {
  display: flex;
  width: 100%;
  text-align: center;
  background-color: #455b86;
  /* Here was changed to fix hover area
   * align-items: center;
  */
  align-items: stretch;
}
.tabs a {
  display: block;
  flex-grow: 1;
  color: #fff;
  background-color: #455b86;
  padding: 15px;
  border-left: 1px solid #fff;
}
.tabs a:hover {
  color: #455b86;
  font-weight: bold;
  background-color: #fff;
  border: 1px solid #455b86;
}
.title {
  width: 100%;
  border-bottom: 0.5px solid #455b86;
}
.news p {
  display: block;
  /* border-bottom: 0.5px solid #181818; */
}
.news p:hover {
  font-weight: bold;
}
.more_btn {
  transform: translate(-100%, 0);
  display: inline-block;
  text-align: right;
  border-radius: 10px;
  color: #455b86;
  padding: 12px 25px;
  margin-left: 100%;
  white-space: nowrap;
}
.more_btn:hover {
  color: #e97142;
  border: 1px solid #e97142;
  font-weight: bold;
  border-radius: 10px;
}
.groups {
  display: flex;
  width: 100%;
}
#activities {
  margin-top: -100px;
  padding-top: 100px;
}

/* GroupCard component is expected to be a direct child of .groups */
.groups > :deep(*) {
  width: 25%;
  text-align: center;
  text-decoration: none;
}

:deep(img) {
  width: auto;
  height: 140px;
  display: block;
  margin: 0 auto 1rem;
}

:deep(.group-card-button) {
  display: inline-block;
  border-radius: 10px;
  color: #455b86;
  padding: 12px 25px;
  text-decoration: none;
}
.groups > :deep(*:hover .group-card-button) {
  background-color: #455b86;
  border-radius: 10px;
  color: #fff;
}

@media screen and (max-width: 1072px) {
  .main_top {
    width: 80%;
    margin-left: 10%;
  }
}
@media screen and (max-width: 670px) {
  .tabs a {
    white-space: nowrap;
    font-size: 14px;
    border-bottom: 1px solid #fff;
  }
  .tabs {
    display: block;
  }
  .groups {
    display: block;
  }
  .groups > :deep(*) {
    width: 100%;
    margin-bottom: 2rem;
  }
}
</style>