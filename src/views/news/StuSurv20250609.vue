<script setup>
import ActivityPageLayout from '../../components/ActivityPageLayout.vue';
import slide1 from '../../assets/images/news/20250609_stusurv/poster.png';
import SlideShow from '../../components/SlideShow.vue';

const slides = [
  { imgSrc: slide1, altText: '', caption: '' },
];
const pageData = {
  title: '学勢調査2024提言報告会を実施します',
};
</script>

<template>
  <ActivityPageLayout :title="pageData.title" :description="pageData.description">
    <template #slideshow>
      <SlideShow :slides="slides" />
    </template>
    <template #details>
      <h3>◇概要</h3>
      <p>
        <b>日時：</b>2025年7月14日（月）17:20～18:20<br>
        <b>対象：</b>本学の学生、教職員（学勢調査に回答していない方や医歯学系の学生・教職員も大歓迎です！）<br>
        <b>参加形式：</b>対面とオンラインのハイブリッド開催<br>
        <b>対面会場：</b>Taki Plaza 大階段エリア(対面の場合は予約不要)<br>
        <b>オンライン：</b>Zoom Webinarにて開催、登録は<a href="https://zoom.us/webinar/register/WN_V28S5Ii2QUmAQ4ZNjCzF_A">こちら</a>から<br>
        ※途中入退場可<br><br>
        学勢調査2024の提言について、学生スタッフから説明いたします。
        <br>報告会の中では、学勢調査に関する質疑応答の時間を設けております。
        <br>学勢調査2024に回答されている方も、されていない方も、医歯学系の学生・教職員も、ぜひご参加ください。
      </p>
      <h3>◇学勢調査の概要</h3>
      <p>
        本学学生(旧東工大生)に対し、全学的アンケート調査「学勢調査」を2年に1度実施しています。 調査項目の設定、 調査結果の集計・解析・提言書作成を学生スタッフ主導で実施しています。 学生の視点で読み解いた アンケート結果を建設的な提言書として作成し、 理事長・学長をはじめとする大学上層部に直接奉呈します。
      </p>
      <h3>◇学勢調査2026スタッフ募集</h3>
      <p>学勢調査では、次回調査である学勢調査2026に向け、学生スタッフを募集中です！ 本報告会では、学生スタッフの活動や応募方法についても説明いたします。 ご興味のある方はぜひご参加ください。<br>
        詳細は<a href="https://www.siengp.titech.ac.jp/gakuseichousa/">こちら！！</a>
      </p>
    </template>
  </ActivityPageLayout>
</template>

<style scoped>
</style>