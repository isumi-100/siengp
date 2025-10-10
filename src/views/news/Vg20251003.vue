<script setup>
import ActivityPageLayout from '../../components/ActivityPageLayout.vue';
import SlideShow from '../../components/SlideShow.vue';

import slide1 from '../../assets/images/news/20251003_vg/hijoushoku.jpg';

const slides = [
  { imgSrc: slide1, altText: '非常食ワークショップポスター', caption: '' },
];

const pageData = {
  title: '10/17(金)17:30~　非常食ワークショップ【参加者募集】',
  description: '　こんにちは！東京科学大学学生ボランティアグループ（VG）です！',
};
</script>

<template>
  <ActivityPageLayout :title="pageData.title" :description="pageData.description">
    <template #slideshow>
      <SlideShow :slides="slides" />
    </template>
    <template #details>
      <p>
        　10/17(金)に開催される「非常食ワークショップ」のお知らせです。
          <br/>大規模災害が発生したときのため、食料の備蓄が推奨されている一方で、こんなことを感じたことはありませんか？
          <br><br>「非常食が重要なのはわかるけど、何をどれくらい用意すれば良いの？」
          <br>「非常食って美味しいの？味が想像しにくくて、買うのが億劫...」
          <br><br>　そこで、東京科学大学学生ボランティアグループ(VG)は、防災活動を行う学生団体Kitmeeと共催で「非常食ワークショップ」を開催します！
          <br>　ワークショップでは、非常食を揃えるにあたってベースとなる考え方を紹介しつつ、色々な非常食の食べ比べを行います。試食できる非常食は、ご飯・パン・ハンバーグなど色々な種類を用意しています。
          <br>　防災について知りたい方、一人暮らしをしていて災害時への不安がある方、非常食の味に興味がある方、様々な方のご参加をお待ちしています！
      </p>
      <p><b style="text-decoration: line-through;">参加登録は<a href="https://forms.gle/WFX1GVh7xKBHKBHX6">こちら<span class="material-symbols-outlined open_in_new_icon">
open_in_new
</span></a>から</b><span style="color: red;"> 申込は締め切りました</span></p>
      <h3>〈開催概要〉</h3>
      <p>日時：10/17(金) 17:30-19:00<br/>
        場所：大岡山キャンパス Taki Plaza 地下2階
        <br>定員：15名（先着順）
        <br/>共催：東京科学大学学生ボランティアグループ(VG)・Kitmee
        <br/>協力：東京科学大学 総務企画部 環境安全課 安全企画グループ
      </p>
    </template>
  </ActivityPageLayout>
</template>

<style scoped>
</style>