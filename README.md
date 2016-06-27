hands-on-vuejs-vol2
===================

## Web Components とは？

- Web の再利用可能なパーツ作成の仕様。


### 再利用可能なパーツを考える上での悩み

- HTML, CSS, JavaScript 3つの専用言語で構成。
- HTML の複雑な入れ子構造
- CSS の意図しない適用範囲
- JavaScript のDOM構造への依存


### 利用のメリット

- マークアップがスッキリ
- スタイルの適用範囲を絞り込む
- 複雑な構造を外部から見えなくする


### 構成するリソース

1. Shadow DOM
2. HTML Imports
3. HTML Template
4. Custom Elements


### ブラウザ対応状況

http://webcomponents.org/

- Google 主導でブラウザベンダの足並みバラバラ
- Polyfill は製品で実装実績がとても少ない
- Polymer, X-Tag などのライブラリでも…
- 開発から4年でそろそろ？
- Vue.js ならば…


## Vue.js と Web Components

- 2つの重要なコンセプト
  - リアクティブデータバインディング
  - コンポーネントシステム


### Vue.js のコンポーネントシステム

Custom Elements の仕様に沿った構文を実装

- slot 要素
- is 属性


### 大規模アプリケーション例

```
<div id="app">
  <app-nav></app-nav>
  <app-view>
    <app-sidebar></app-sidebar>
    <app-content></app-content>
  </app-view>
</div>
```

![http://jp.vuejs.org/images/components.png](http://jp.vuejs.org/images/components.png)
