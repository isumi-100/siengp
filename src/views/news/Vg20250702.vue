<script setup>
import ActivityPageLayout from '../../components/ActivityPageLayout.vue';
import SlideShow from '../../components/SlideShow.vue';

import slide1 from '../../assets/images/news/20250702_vg/image1.jpg';
import slide2 from '../../assets/images/news/20250702_vg/image2.jpg';
import slide3 from '../../assets/images/news/20250702_vg/image3.jpg';

const slides = [
  { imgSrc: slide1, altText: '物産展の様子1', caption: '物産展の様子1' },
  { imgSrc: slide2, altText: '物産展の様子2', caption: '物産展の様子2' },
  { imgSrc: slide3, altText: '物産展の様子3', caption: '物産展の様子3' },
];

const pageData = {
  title: '【VG】ホームカミングデイ in 大岡山にて復興支援物産展を開催',
  description: '　東京科学大学学生ボランティアグループ(以下、VG)は、5月24日(土)の「ホームカミングデイ in 大岡山」に合わせて、復興支援物産展を開催しました。この物産展は、VGの活動目的の1つである、復興活動支援の一環として行われ、被災県の物産館から仕入れた商品を販売しています。同時に、VGが行っている取り組みや、復興活動支援以外の活動を紹介したポスターも展示し、VGの活動が広く知っていただけるように取り組んでいます。',
};
</script>

<template>
  <ActivityPageLayout :title="pageData.title" :description="pageData.description">
    <template #slideshow>
      <SlideShow :slides="slides" />
    </template>
    <template #details>
      <p>
        　物産展は基本的に仕入れ値で販売していますが、皆様にお買い求めいただきやすいようばら売りしているため、若干の差額が生じています。その差額分を含め仕入れ値は全て被災地に還元しています。また、物産展とは別に能登半島復興支援に向けた、日本赤十字への募金箱も設置しました。<br><br>
        　今回は、石川県と福島県の商品を取り上げ、石川県からは老舗店の和菓子や能登の海産物を使った製品などを、福島県からは地元の生ラーメンや桃を使ったお菓子などを販売しました。当日は多くのお客様に来訪いただき、売上差額は1,295円、募金額は6,550円に達し、合計7,845円を日本赤十字社へ寄付しました。また、お客様から多くのご厚意と激励の声をいただき、我々VGとしても、今後の励みとなると同時に、改めて身が引き締まる思いがしました。<br><br>
        　ホームカミングデイに引き続き、今年11月2日(日)と3日(月・祝)の工大祭に合わせて、物産展を両日とも開催する予定です。工大祭でもお客様に喜んでいただけるような物産展となるよう、VG一同準備を進めています。
      </p>
    </template>
  </ActivityPageLayout>
</template>

<style scoped>
</style>