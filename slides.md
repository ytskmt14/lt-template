---
# try also 'default' to start simple
theme: seriph
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

# Gemを作ってみたお話

---
layout: image-right
image: ./my-profile.jpg
class:
---

坂元　ゆーた <mdi-twitter/> @sorigeeeen

<div class="leading-10">
  <div class="list-margin">
    <p>
      <dashicons-businessman/> バックエンドエンジニア
    </p>
  </div>
  <div class="list-margin">
    <p><dashicons-businessman/> エンジニア６年生</p>
    <ul>
      <li class="list-none"><simple-icons-rubyonrails class="text-3xl"/> ２年</li>
      <li class="list-none"><simple-icons-java class="text-3xl"/> ２年</li>
      <li class="list-none"><simple-icons-php class="text-3xl"/> １年</li>
    </ul>
  </div>
  <div class="list-margin">
    <p><bx-bxs-like/> 珈琲</p>
  </div>
  <div class="list-margin">
    <p><bx-bxs-like/> サッカー&フットサル</p>
  </div>
</div>

<style>
  .list-margin {
    @apply my-5
  }
</style>

---
layout: image-right
image: ./coffee_1.jpg
class: text-center flex items-center
---

# caffè e llatte <br/> x <br/> chocolate sauce <br/> x <br/> caramel sauce

---
layout: image-right
image: ./coffee_4.jpg
class: text-center flex items-center
---

# caffè e llatte <br/> x <br/> chocolate sauce <br/> x <br/> caramel sauce

---
layout: image-right
image: ./coffee_2.jpg
class: text-center flex items-center
---

# caffè e llatte

---
layout: fact
---

# さて、本題です

---
layout: fact
---

# Gem、、、？

---
layout: quote
---

> 多くのプログラミング言語と同様に、Ruby にも幅広いサードパーティのライブラリが提供されています。
> それらのほとんどは “gem” という形式で公開されています。RubyGems は (Ruby に特化した apt-get と同じようなパッケージングシステムで) ライブラリの作成や公開、インストールを助けるシステムです。Ruby のバージョン 1.9 以降 RubyGems は標準添付となっていますが、それ以前のバージョンの Ruby の場合は自分でインストールする必要があります。

<div class="my-5 text-right">
  <a href="https://www.ruby-lang.org/ja/libraries/">公式サイト</a>より引用
</div>

---
layout: center
---

## Gem作った <br/> = Rubyで使えるライブラリ作った

---
layout: fact
---

# connpass_event

---
layout: iframe-right
url: https://connpass.com/about/api/
class: leading-5 grid content-center
---
# connpass_eventとは？

* connpassのイベント情報取得を楽にするもの

* 公開されているconnpass APIを利用


---
layout: default
---
# モチベーション

* Gem（ライブラリ）の作り方を知りたい

  * ~~作れたらなんかかっこいい~~

* rubyチョットデキルようになりたい

* connpassからイベント情報を楽に取得したい

---
layout: iframe-right
url: https://rubygems.org/gems/connpass_event
class: grid content-center
---
# こんなのができた

---
layout: fact
---

# このGemで<br/>何が変わるのか

---
layout: default
---
# before

```ruby
require 'faraday'

connection = Faraday.new(url: 'https://connpass.com/api/v1/')
connection.params = { 'owner_nickname': 'sorigeeeen'}
response = connection.get('event/')

pp JSON.parse(response.body)['events']
```
<br/><br/>


# after
```ruby
require 'connpass_event'

client = ConnpassEvent::Client.new
params = ConnpassEvent::Request.params(owner_nickname: 'sorigeeeen')

pp client.events(params)
```

---
layout: fact
---
# いい感じ（自己満）

---
layout: iframe-right
url: https://rubygems.org/gems/connpass
---

# 本家のものはある

* 今回作成するにあたって存在は把握していた

* 敢えてドキュメントやソースは見ないようにしてた


---
layout: fact
---

# 本家の使い方と比較

---
layout: default
---
# 本家(connpass)

```ruby
require 'connpass'

res = Connpass.event_search(owner_nickname: 'sorigeeeen')

pp res.events
```
<br/><br/>


# 作ったやつ(connpass_event)
```ruby
require 'connpass_event'

client = ConnpassEvent::Client.new
params = ConnpassEvent::Request.params(owner_nickname: 'sorigeeeen')

pp client.events(params)
```

---
layout: fact
---
# 本家の方で<br/>よくね、、？ww

---
layout: default
---
# まとめ

* はじめてGemを作ってみた

* クオリティはともかく作るだけなら簡単

* せっかく作ったからもうちょっとそれらしくしていきたい

* そのうちzennとかで詳細記事出します

---
layout: image
image: ./musubite.jpg
---
