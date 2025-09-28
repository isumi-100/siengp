<script setup>
import ActivityPageLayout from '../components/ActivityPageLayout.vue';
import SlideShow from '../components/SlideShow.vue';

import logo from '../assets/images/flap/logo.jpg';
import slide1 from '../assets/images/flap/fair_booth.webp';
import slide2 from '../assets/images/flap/event.webp';

const slides = [
  { imgSrc: slide1, altText: '留学フェアでのブース対応', caption: '留学フェアでのブース対応' },
  { imgSrc: slide2, altText: 'FLAP主催の国際交流促進イベント', caption: 'FLAP主催の国際交流促進イベント' },
];

const pageData = {
  title: '留学促進団体FLAP',
  description: '東京科学大生の留学支援を目的とした学生団体です。「全ての東京科学大生にとって『留学』が当たり前の選択肢になること」を目標に、 HP作成・個別相談・イベント開催・SNSの発信等を行っています。',
  logo: logo
};
</script>

<template>
  <ActivityPageLayout :title="pageData.title" :description="pageData.description" :logo="pageData.logo">
    <template #slideshow>
      <SlideShow :slides="slides" />
    </template>
    <template #details>
      <h3>◇FLAP HP・SNS</h3>
      <ul>
        <li>
          FLAPのHPは<a href="https://www.flap-sciencetokyo.com/">こちら</a
          >をご覧ください。
        </li>
        <li>
          <a href="https://twitter.com/FLAP_TokyoTech">X（旧Twitter）</a>
        </li>
        <li>
          <a href="https://www.instagram.com/flap_sciencetokyo/">Instagram</a>
        </li>
      </ul>
    </template>
  </ActivityPageLayout>
</template>