<script setup>
import ActivityPageLayout from '../../components/ActivityPageLayout.vue';
import SlideShow from '../../components/SlideShow.vue';

import slide1 from '../../assets/images/news/20250602_kikai/1.webp';
import slide2 from '../../assets/images/news/20250602_kikai/2.webp';
import slide3 from '../../assets/images/news/20250602_kikai/3.webp';
import slide4 from '../../assets/images/news/20250602_kikai/4.webp';
import slide5 from '../../assets/images/news/20250602_kikai/5.webp';
import slide6 from '../../assets/images/news/20250602_kikai/6.webp';

const slides = [
  { imgSrc: slide1, altText: 'Maker Faire Tokyoの出展ブースの様子', caption: '1.Maker Faire Tokyoの出展ブースの様子' },
  { imgSrc: slide2, altText: '開催したワークショップで作品を真剣に組み立てる小学生', caption: '2.開催したワークショップで作品を真剣に組み立てる小学生' },
  { imgSrc: slide3, altText: '辰の彩色作業', caption: '3.辰の彩色作業' },
  { imgSrc: slide4, altText: '完成した辰のデザイン', caption: '4.完成した辰のデザイン' },
  { imgSrc: slide5, altText: '瓶の中のオルゴール', caption: '5.瓶の中のオルゴール' },
  { imgSrc: slide6, altText: 'イタリアでのワークショップの様子', caption: '6.イタリアでのワークショップの様子' },
];

const pageData = {
  title: 'みらい創造チャレンジ 瓶の中の機械ワークショップ',
  description: '代表　斎藤 天丸 (工学院 機械系 機械コース)',
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
        「ボトルシップを瓶の中で動かしたい！」そんなテキトーな思いから始まった私たちのプロジェクトは思いもよらない発展を遂げ，ついには海外展開を果たしました。
        <br />私たちは第1期からみらい創造チャレンジのご支援をいただき，瓶の中で動く機械を組み立てるという新しい技術・アートにチャレンジしてきました．第3期では
        この "からくり瓶"
        をより一層外へ広げることに着目し，「多くの人と出会う」「対象年齢を広げる」「広報活動」の
        3 つの軸を中心に進めてきました．
        <br />「多くの人と出会う」に関して，Maker Faire Tokyo に "からくり瓶"
        出展しました．中には商品化を望む声もあり，新たな視点を得る機会にもなりました．また，瓶の中で電子回路を組まれていた方など，似た志を持つ
        Maker さんとも出会うこともできました．
        <br />「対象年齢を広げる」に関しては，同じくみらい創造チャレンジの「おおお知る街プロジェクト」様とのコラボの中で，大岡山商店街にてワークショップを開催しました．3
        歳の方から小学校高学年の方まで幅広く "からくり瓶"
        の製作を体験いただけ，特に小さいお子さんのパッションには魅せられるものがありました．
        <br />「広報活動」に関しては、ブログを開設して記事の執筆を行ったり，2024
        年の干支である辰をモチーフにした機構を PV に収めて YouTube Shorts
        に投稿したりしました．
        <br />
        <a href="https://oksroom.com/" target="_blank" rel="noopener noreferrer">ブログはこちら</a>
        <br /><a
          href="https://youtube.com/shorts/Kk2gr7KVyaw?si=Czw7GbcV0a3daGT6"
          target="_blank" rel="noopener noreferrer"
          >Youtube Shortsはこちら</a
        >
        <br /><br />
        こうした活動が新たな繋がりを生み，第3期が満了した後も様々な活動を続けています．
        <br />狭山金型製作所様とコラボ開発して実現した瓶の中のオルゴールは微細加工コンテストにて優勝を頂くことができました．
        <br />
        <a href="https://www.youtube.com/watch?v=-8Pbo23M9Wk" target="_blank" rel="noopener noreferrer">オルゴールについての動画はこちら</a>
        <br /><a
          href="https://bisai-monozukuri.com/lp/expert-bisai-creators/entrywork2024.html"
          target="_blank" rel="noopener noreferrer"
          >コンテストページはこちら</a
        >
        <br /><br />
        また，イタリアの大学でもワークショップを開催し，"からくり瓶"は世界進出を果たしました．
        <br />今後も新しい繋がりを求めてチャレンジを続けていきたいと思っております．今後とも"からくり瓶"をどうぞ宜しくお願い致します．
      </p>
      <h3>◇みらい創造チャレンジからの支援についてのコメント</h3>
      <p>
        みらい創造チャレンジの魅力はプロジェクトの結果ではなく，過程をとても大切にしてもらえることです．プロジェクトの最初の一歩はときに不確実で，何が起こるか分かりません．一般的な資金援助プログラムなら，最終発表の際になぜ思うような結果が出なかったのかを問われることでしょう．一方でみらい創造チャレンジは応援して下さる先生方に定期的にプロジェクト進捗を相談する機会があります．確かに専門的な工学の知識はプロジェクトメンバーのほうが詳しいかもしれません．しかし，不確実性の高い最初の一歩だからこそ，客観的な様々な分野の視点は大切です．私たちのプロジェクトもこうしたメンタリングを繰り返し，申請当初とは全く異なるプロジェクトに成長していきました．そうした柔軟性のある雰囲気もこのチャレンジの魅力です．
      </p>
      <h3>◇後輩学生へのメッセージ</h3>
      <p>
        皆さんは何か「変な」アイディアを持ってはいませんか？そしてそのアイディアを育ててみたいと密かに思ったことはありませんか？アイディアは自分の中で温めているだけではなかなか成長しません．しかし，ひとたび外の世界に出してみれば，"からくり瓶"のように自分でも思いもよらない結果が待っているかもしれません．思いきって最初の一歩を踏み出してみては如何でしょうか．
      </p>
    </template>
  </ActivityPageLayout>
</template>

<style scoped>
</style>