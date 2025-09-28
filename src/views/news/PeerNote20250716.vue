<script setup>
import img1 from '../../assets/images/peer/fig4.jpg';
import img2 from '../../assets/images/peer/fig5.jpg';
import img3 from '../../assets/images/peer/fig6.jpg';
</script>
<template>
  <div class="main">
    <div class="introduction">
      <h3>「ぐるっと！！ぴあノート」概要</h3>
      <p>
        「ぐるっと！！ぴあノート」は、大岡山キャンパス、すずかけ台キャンパス、湯島キャンパスの3つのキャンパスをめぐるつぶやき帳です。
        <br />　ピアちゃんのリプライ箱とは違って、ピアサポーターからのおへんじはありません。誰かに話したい日常の些細な出来事、自分が過ごすキャンパスのおすすめポイント、他キャンパスへのメッセージなど、キャンパスを超えて自由に書き込んでいただければと思います。
        <br />　このノートは本学の学生及び教職員の方ならどなたでもご自由にご記入いただけます。皆様の素敵な書き込みをお待ちしています！
      </p>
      <h3>設置場所</h3>
      <p>　大岡山キャンパス　Taki Plaza B1階</p>
      <img :src="img1" class="image" alt="Taki Plaza" />
      <p>　すずかけ台キャンパス　大学会館3階 ラウンジ入口</p>
      <img :src="img2" class="image" alt="すずかけ台" />
      <p>　湯島キャンパス　M&Dタワー3F お茶の水図書館前 飲食ラウンジ内</p>
      <img :src="img3" class="image" alt="湯島" />

      <h3>記入にあたってのお願い</h3>
      <ul>
        <li>写真撮影はご遠慮ください</li>
        <li>誹謗中傷、個人情報などは書かないでください。</li>
        <li>内容をSNSなどで公開しないでください。</li>
        <li>ノートやペンは大切に扱ってください。</li>
      </ul>
    </div>
  </div>
</template>

<style scoped>

.image {
  max-width: 80%;
  margin-left: 10%;
  height: auto;
  margin-bottom: 1rem;
}
</style>