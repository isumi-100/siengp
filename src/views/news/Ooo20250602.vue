<script setup>
import ActivityPageLayout from '../../components/ActivityPageLayout.vue';
import SlideShow from '../../components/SlideShow.vue';

import slide1 from '../../assets/images/news/20250602_ooo/event.webp';
import slide2 from '../../assets/images/news/20250602_ooo/tour.webp';
import slide3 from '../../assets/images/news/20250602_ooo/communication.webp';

const slides = [
  { imgSrc: slide1, altText: '商店街での主催イベント『飛び出せ！おおお知るまちプロジェクト』', caption: '商店街での主催イベント『飛び出せ！おおお知るまちプロジェクト』' },
  { imgSrc: slide2, altText: 'まちの方へのキャンパスツアーの様子', caption: 'まちの方へのキャンパスツアーの様子' },
  { imgSrc: slide3, altText: 'イベントを通してまちの方との交流が生まれます', caption: 'イベントを通してまちの方との交流が生まれます' },
];

const pageData = {
  title: 'みらい創造チャレンジ おおお知るまちプロジェクト',
  description: '代表　小倉 達也 (環境社会理工学院 建築学系 都市環境学コース)',
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
        大岡山の魅力の発信を目的に、ブログサイト『note』での記事執筆や、種々のイベントを開催しています。
        おおお（大岡山）のまちについて科学大生やまちの方にもっと知ってもらいたい、そして私たちがもっと知りたい！という想いで活動しています。
        昨年度は商店街での大岡山に関する展示や大岡山夏みかんジャム作り、まちの方に向けたキャンパスツアーなどを行い、イベントでは科学大生にまちの方向けに研究発表をしてもらいました。
        詳しい私たちの活動については<a href="https://note.com/oooshirumachi" target="_blank" rel="noopener noreferrer"><b>note</b></a>からぜひご覧ください！
      </p>
      <h3>◇みらい創造チャレンジからの支援についてのコメント</h3>
      <p>
        活動のための助成をいただいたのみならず、活動について定期的に確認や報告の機会を設けていただきました。その都度我々が目的としていること、挑戦してみたいと思っていることを振り返り、そこへ向けた道筋を確認することができました。
        <br />3期にわたり、みらい創造チャレンジのご支援をいただきながら、本プロジェクトは発足から発展、そして引き継ぎへとつながるプロセスを経てきました。今後もこのプロジェクトを続けていくことをできたらなと思います。ご支援いただき、ありがとうございました。
      </p>
      <h3>◇後輩学生へのメッセージ</h3>
      <p>
        何かチャレンジしたいと思うことがあるのであれば、ぜひとも一歩踏み出してみましょう。そして、周りに面白いことを始めようとする動きがあれば、ぜひ参加してみましょう。みらい創造チャレンジでは、あなたと同じく何かにチャレンジしようとしている人たちに出会うことができます。
      </p>
    </template>
  </ActivityPageLayout>
</template>

<style scoped>
</style>