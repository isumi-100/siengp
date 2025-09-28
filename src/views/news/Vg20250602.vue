<script setup>
import ActivityPageLayout from '../../components/ActivityPageLayout.vue';
import slide1 from '../../assets/images/news/20250602_vg/picture.jpg';
import SlideShow from '../../components/SlideShow.vue';
import posterPdf from '../../assets/files/news/kokuchi_R7_0520_0018.pdf';

const slides = [
  { imgSrc: slide1, altText: '', caption: '' },
];
const pageData = {
  title: '【VG】フィルム上映会「LIGHT UP NIPPON～日本を照らした奇跡の花火～」を開催（2025/6/13）',
  description: '<b>日時：</b>2025年6月13日（金）18:00～19:30<br><b>場所：</b>タキプラザ地下2階イベントスペースにて<br><b>対象：</b>東京科学大学の学生・教職員<br><b>参加方法：</b>無料(事前申込不要)<br></br>学生ボランティアグループ（VG）がフィルム上映会を開催します。<br>皆さま、ぜひご覧ください。',
};
</script>

<template>
  <ActivityPageLayout :title="pageData.title" :description="pageData.description">
    <template #slideshow>
      <SlideShow :slides="slides" />
    </template>
    <template #details>

      <h3>◇『LIGHT UP NIPPON』のあらすじ</h3>
      <p>
        2011年3月11日に起きた東日本大震災。未曾有の地震と津波による膨大な被害を目の前に、日本中の誰もが下を向き、日本がこの先どうなっていくのか不安を抱いていた。そんな中、たった一人の男の「いつまでも下を向いていられない」という信念のもと立ち上がった、「LIGHT UP NIPPON」プロジェクト。その内容とは、東北太平洋沿岸部10ヶ所での花火同時打ち上げであった。
      </p>
      <p><b><a :href="posterPdf" target="_blank" rel="noopener noreferrer">告知ポスターはこちら</a></b></p>
    </template>
  </ActivityPageLayout>
</template>

<style scoped>
</style>