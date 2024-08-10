---
# You can also start simply with 'default'
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# some information about your slides (markdown enabled)
title: ふんわりLT 20240811
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
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

# Lambda の設定について簡単に

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

<style>
p {
  font-size: 24px;
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

- ドキュメント通りのメモリが倍になると CPU の速度も倍になる
- CPU 依存のプログラムの場合はメモリ設定を大きめにとったほうがコストが低くなる可能性がある
- プロビジョニングするときは課金システムが変わるので注意

<style>
li {
  font-size: 24px;
}
</style>