<script setup>
import ActivityPageLayout from '../../components/ActivityPageLayout.vue';
import SlideShow from '../../components/SlideShow.vue';

import slide1 from '../../assets/images/news/20250515_kitmee/bousai.jpg';
import slide2 from '../../assets/images/news/20250515_kitmee/field.png';

const slides = [
  { imgSrc: slide1, altText: 'Kitmeeの活動の様子1', caption: 'Kitmeeの活動の様子1' },
  { imgSrc: slide2, altText: 'Kitmeeの活動の様子2', caption: 'Kitmeeの活動の様子2' },
];

const pageData = {
  title: 'みらい創造チャレンジ Kitmeeプロジェクト',
  description: '代表　高橋 遼 (工学院 機械系)',
};
</script>

<template>
  <ActivityPageLayout :title="pageData.title" :description="pageData.description">
    <template #slideshow>
      <SlideShow :slides="slides" />
    </template>
    <template #details>
      <h3>◇プロジェクト概要</h3>
      <p>
        Kitmeeは、子どもたちがプログラミングを学ぶための新しい方法を提案するプロジェクトです。私たちは、子どもたちが自分の手で組み立てたものが、プログラミングによって動くという体験を提供したいと考えています。この体験を通して、子どもたちがプログラミングに興味を持ち、創造性を育むことを目指しています。
      </p>
      <h3>◇みらい創造チャレンジからの支援についてのコメント</h3>
      <p>
        みらい創造チャレンジの支援により、私たちはKitmeeのプロトタイプを開発し、多くの子どもたちに体験してもらうことができました。メンターの方々からのアドバイスは、プロジェクトを進める上で非常に役立ちました。この経験を活かし、今後も子どもたちのための教育ツールを開発していきたいと考えています。
      </p>
      <h3>◇後輩学生へのメッセージ</h3>
      <p>
        自分のアイデアを形にしたいと思ったら、ぜひみらい創造チャレンジに応募してみてください。資金的な支援だけでなく、多くの人との出会いや学びの機会が得られます。失敗を恐れずに、挑戦することが大切です。
      </p>
    </template>
  </ActivityPageLayout>
</template>

<style scoped>
</style>
