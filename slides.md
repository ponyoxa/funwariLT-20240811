---
# You can also start simply with 'default'
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# some information about your slides (markdown enabled)
title: ふんわりLT 20240811
info:
# apply unocss classes to the current slide
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
layout: image-right
image: ./img/icon.png
---

# 自己紹介

ponyoxa です

TypeScript メインのバックエンドエンジニア

キーボードが好き。自作キーボードを組みたい今日このごろ

---
layout: center
transition: slide-left
---

ところでみなさん

AWS Lambda は使ったことがありますか？

---
layout: default
transition: slide-left
---

# Lambda の設定について簡単に

- メモリサイズを設定する

- 実行時間課金

---
layout: quote
transition: slide-left
---

# 公式ドキュメントには...

> Lambda は、設定されたメモリの量に比例して CPU パワーを割り当てます。


---
layout: default
transition: slide-left
---

ほんとですか？ 

---
layout: default
transition: slide-left
---

# 実験してみた

---
layout: default
transition: slide-left
---

# 結果をざっくり

---
layout: default
transition: slide-left
---

# 結論

- ドキュメント通りのメモリが倍になると CPU の速度も倍になる
- CPU 依存のプログラムの場合はメモリ設定を大きめにとったほうがコストが低くなる可能性がある
- プロビジョニングするときは課金システムが変わるので注意

