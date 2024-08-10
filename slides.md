---
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# some information about your slides (markdown enabled)
title: ふんわりLT 20240811
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
---

# AWS Lambda のメモリ設定、損してませんか？

ponyoxa

@1周年！若手エンジニアふんわりLT Day！

---
transition: slide-left
layout: default
---

# 自己紹介
<br>

ponyoxa です、ぽにょって読んでください

TypeScript メインのバックエンドエンジニア

<br>

キーボードが好き。自作キーボードを組みたい今日このごろ

秋葉原付近をうろうろするのが好き

爬虫類も好き

アイコンは従妹に描いてもらいました

初めて slidev でスライドを作ったけどあまり使いこなせなかった orz

初めての LT !!

<img src="./img/icon.png" class="absolute top-40 right-10 w-60">

<style>
p {
  font-size: 22px;
}
</style>

---
layout: center
transition: slide-left
---

<div class="text-4xl">
ところでみなさん
<br>
<br>AWS Lambda は使ったことがありますか？
</div>

---
layout: default
transition: slide-left
---

# Lambda について簡単に

<div class="text-2xl">

- メモリサイズを設定する

- 実行時間課金

</div>


---
layout: quote
transition: slide-left
---

# 公式ドキュメントには...

<br>

> Lambda は、設定されたメモリの量に比例して CPU パワーを割り当てます。

<div class="citation absolute bottom-5">
引用：https://docs.aws.amazon.com/ja_jp/lambda/latest/dg/configuration-memory.html
</div>

<style>
p {
  font-size: 24px;
}

.citation {
  font-size: 16px
}
</style>

---
layout: center
transition: slide-left
---

ほんとですか？<emojione-thinking-face/>

<style>
p {
  font-size: 50px;
}
</style>


---
layout: default
transition: slide-left
---

# 実験してみた

- Node ランタイム
- 外部と連携しない CPU 依存なプログラム
- プログラムが使用するメモリは 100MB 程度で、メモリ設定だけでいうと 256MB で十分

<br>

- 256MB, 512MB, 1024MB で設定
  - 実行時間の比較
  - コストの比較

<style>
li {
  font-size: 24px;
}
</style>

---
layout: default
transition: slide-left
---

# 結果をざっくり その1
<br>

メモリ設定と実行時間の関係

<img src="./img/lambda-graph.png">


---
layout: default
transition: slide-left
---

# 結果をざっくり その2
<br>

コストはどうだったか

<img src="./img/lambda-cost.png">

---
layout: default
transition: slide-left
---

# 結論

- ドキュメント通り、メモリが倍になると CPU の速度も倍になる
- CPU 依存のプログラムの場合はメモリ設定を大きめにとったほうがコストが低くなる可能性がある
- プロビジョニングするときは課金システムが変わるので注意

<style>
li {
  font-size: 24px;
}
</style>

---
layout: center
transition: slide-left
---

おわり！

<br>

2025年3月9日(日)に「エンジニアがこの先生きのこるためのカンファレンス」をやります！

コアスタッフやってます。ぜひ X のフォローしてください。
@kinoko_conf

<style>
p {
  font-size: 24px;
}
</style>