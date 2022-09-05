---
# try also 'default' to start simple
theme: bricks
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: true
# persist drawings in exports and build
drawings:
  persist: false
---

# LT資料のテンプレートを<br/>作り始めたお話

---
layout: TwoColWithHeader
---
::default::
<!-- ./components/ContentHeader -->
<ContentHeader text="Speaker" />

::left_column::
<ContentList :items="['坂元　佑太 (31)', 'バックエンドエンジニア@福岡']" />

<div class="my-3 text-3xl font-bold">最近のTopics</div>
<ContentList :items="['作業用の椅子をバランスボールに変えました', 'Ruby Kaigiがもうすぐあることを知る', 'Kaigi on Railsももうすぐあることを知る']" />

::right_column::
<img src="logo-slidev.png"/>

---
layout: iframe
url: https://rubykaigi.org/2022/
---
# Ruby Kaigi

---
layout: iframe
url: https://kaigionrails.org/2022/
---
# Kaigi on Rails

---
layout: fact
---

# 意外とLTする機会があることに気づいた今日この頃

---
layout: fact
---

# 毎回レイアウト考えたりするのめんどい・・・

---
layout: fact
---

# なんかないかな・・・

---
layout: fact
---

# 気になるのあった
<img src="logo-slidev.png" class="mx-auto h-60">

---
layout: fact
---

# 実はこの資料も<br />Slidev使ってます

---
layout: OneColWithHeader
---

::default::
<!-- ./components/ContentHeader -->
<ContentHeader text="Slidevとは？" />

::content::

<p class="leading-loose text-3xl">Slidev = slide + dev</p>
<p class="leading-loose text-3xl">Webベースのスライド作成＆プレゼンテーションツール</p>
<p class="leading-loose text-3xl">
  <span>2021年5月リリース？(</span>
  <a class="text-blue-700 underline" href="https://github.com/slidevjs/slidev/releases/tag/v0.0.0-alpha.58">v0.0.0-alpha.58</a>
  <span>)</span>
</p>
<p class="leading-loose text-3xl">Markdownで書ける</p>
<p class="leading-loose text-3xl">HTMLやVue.jsも使える</p>
<p class="leading-loose text-3xl">などなど</p>

---
layout: iframe
url: https://ja.sli.dev/guide/#%E6%8A%80%E8%A1%93%E3%82%B9%E3%82%BF%E3%83%83%E3%82%AF
---

---
layout: fact
---

# ここからが本題

---
layout: OneColWithHeader
---

::default::
<!-- ./components/ContentHeader -->
<ContentHeader text="とりあえずリポジトリを作った" />

::content::
<ContentLink text="ytskmt14/lt-template" url="https://github.com/ytskmt14/lt-template" />

<div class="my-3 text-3xl font-bold">概要</div>
<ContentSubText text="カスタムレイアウトの作成"/>
<ContentSubText text="カスタムコンポーネントの作成"/>
<ContentSubText text="README.mdを少し書いた"/>

---
layout: OneColWithHeader
---

::default::
<!-- ./components/ContentHeader -->
<ContentHeader text="カスタムレイアウト①" />

::content::

<div class="grid grid-cols-12 bg-green-500 mb-8 h-15 text-center">
  <span class="text-2xl">Header</span>
</div>
<div class="grid grid-cols-1">
  <div class=" bg-yellow-500 h-80">
  <span class="text-2xl">Main Content</span>
  </div>
</div>

---
layout: OneColWithHeader
---

::default::
<!-- ./components/ContentHeader -->
<ContentHeader text="カスタムレイアウト①" />

::content::

<div class="my-3 text-3xl font-bold">OneColWithHeader.vue</div>

```ts
<template>
  <span class="text-5xl">{{ headerText }}</span>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const props = defineProps({
  text: {
    type: String,
    require: true
  }
})
</script>
```

---
layout: OneColWithHeader
---

::default::
<!-- ./components/ContentHeader -->
<ContentHeader text="カスタムレイアウト②" />

::content::
<div class="grid grid-cols-12 bg-green-500 mb-8 h-15">
  <span class="text-2xl">Header</span>
</div>
<div class="grid grid-cols-2">
  <div class=" bg-yellow-500 h-80">
  <span class="text-2xl">Left Content</span>
  </div>
  <div class=" bg-blue-500">
  <span class="text-2xl">Right Content</span>
  </div>
</div>

---
layout: OneColWithHeader
---

::default::
<!-- ./components/ContentHeader -->
<ContentHeader text="カスタムレイアウト①" />

::content::

<div class="my-3 text-3xl font-bold">TwoColWithHeader.vue</div>

```ts
<template>
  <div class="container mx-auto mt-3 px-8">
    <div class="mb-8">
        <slot/>
    </div>
    <div class="grid grid-cols-2">
      <div>
        <slot name="left_column"/>
      </div>
      <div>
        <slot name="right_column"/>
      </div>
    </div>

  </div>
</template>
```

---
layout: OneColWithHeader
---

::default::
<!-- ./components/ContentHeader -->
<ContentHeader text="まとめ" />

::content::
<p class="leading-loose text-3xl">Markdownで作れるの嬉しい</p>
<p class="leading-loose text-3xl">フロントの理解浅くて辛い</p>
<p class="leading-loose text-3xl">未完成すぎて今日発表するか迷った</p>
<p class="leading-loose text-3xl">次のLTに向けてブラッシュアップします</p>
