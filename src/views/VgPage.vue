<script setup>
import ActivityPageLayout from '../components/ActivityPageLayout.vue';
import SlideShow from '../components/SlideShow.vue';

import logo from '../assets/images/vg/logo.jpg';
import slide1 from '../assets/images/vg/kodomo.jpg';
import slide2 from '../assets/images/vg/studytour.jpg';
import slide3 from '../assets/images/vg/recycle.jpg';
import slide4 from '../assets/images/vg/bussan.jpg';

const slides = [
  { imgSrc: slide1, altText: 'こども食堂の様子', caption: 'こども食堂の様子' },
  { imgSrc: slide2, altText: 'スタディツアーの様子', caption: 'スタディツアーの様子' },
  { imgSrc: slide3, altText: '古本寄付活動・コンタクト空きケース回収活動', caption: '古本寄付活動・コンタクト空きケース回収活動' },
  { imgSrc: slide4, altText: '被災地復興支援物産展の様子', caption: '被災地復興支援物産展の様子' },
];

const pageData = {
  title: '学生ボランティアグループ（VG）',
  description: '復興支援・防災活動・地域連携を軸に、学内外で様々な活動を実施しています。主な活動としては、学祭での復興支援物産展、被災地スタディツアー、学内防災イベント、こども食堂、教科書譲渡の仲介などがあります。学生の提案が新たな企画として成立することもあります！',
  logo: logo
};
</script>

<template>
  <ActivityPageLayout :title="pageData.title" :description="pageData.description" :logo="pageData.logo">
    <template #slideshow>
      <SlideShow :slides="slides" />
    </template>
    <template #details>
      <h3>◇メンバー構成</h3>
      <p>10名程度（2025.4現在）</p>
      <h3>◇活動頻度</h3>
      <p>週1回昼休みにミーティング</p>
      <h3>◇参加について</h3>
      <p>
        一年中、学年問わず（B1〜D3）募集しています！<br />お気軽にご連絡ください。
      </p>
      <h3>◇連絡先</h3>
      <ul>
        <li><a href="https://x.com/titechvg">X(旧twitter)</a></li>
        <li>
          <a href="https://www.instagram.com/tokodai_vg/">Instagram</a>
        </li>
      </ul>
    </template>
  </ActivityPageLayout>
</template>