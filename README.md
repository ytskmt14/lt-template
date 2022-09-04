# LT資料用のテンプレート

## はじめかた
```bash
# clone repository
$ git clone git@github.com:ytskmt14/lt-template.git
# or
$ git clone https://github.com/ytskmt14/lt-template.git

# package install
$ cd lt-template
$ yarn

# start your presentation
$ yarn dev

# and visit http://localhost:3030
```

## 概要
[Slidev](https://sli.dev/)に、オレオレカスタムコンポーネントとカスタムレイアウトを追加しているだけのリポジトリです。

## カスタムレイアウト
追加したカスタムレイアウトについて。

### OneColWithHeader
ヘッダー付き1カラム構成用のレイアウト。

```md
---
layout: OneColWithHeader
---
::default::
ヘッダーコンテンツ

::content::
メインコンテンツ
```

### TwoColWithHeader

```md
---
layout: TwoColWithHeader
---

::default::
ヘッダーコンテンツ

::left_column::
左側のコンテンツ

::right_column::
右側のコンテンツ
```

## カスタムコンポーネント
追加したカスタムコンポーネントについて。

### ContentHeader
ヘッダーテキスト表示用コンポーネント。

```md
<ContentHeader text="ヘッダー用テキスト" />
```

### ContentList
リスト表示用コンポーネント。

```md
<ContentList :items="['item A', 'item B', 'item C']" />
```
