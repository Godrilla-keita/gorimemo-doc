# 設計

## 構成
### バックエンド
* Java SE 17 (Open JDK)
  * v0.0.0
* Spring Boot
  * v0.0.0

### フロントエンド
* vue.js
  * v0.0.0
* vuetify
  * v0.0.0
* 

## データベース設計
[詳細はこちら](./database-design/index.md)

## 画面設計
* [サンプル画面](./screen-layout/template.md)
* この下に画面を追加していく

## 画面遷移図
[詳細はこちら](./transition-diagram/index.md)

## API設計

[詳細はこちら](./api-design/index.md)

### 編集方法

`OpenAPI`という記法で書かれた`yml`ファイルを書いていく。

### OpenAPIをmarkdownに変換する方法
[node公式ページ](https://nodejs.org/ja/download)からインストーラをダウンロードし、インストールする。

nodeがインストールできると、npmコマンドを使用できる。`widdershins`というツールをダウンロードし、変換を実行する。

```sh
# インストール
npm i -g widdershins

# 変換実行
npx widdershins --omitHeader --code true .\api-design\index.yml .\api-design\index.md
```

### API設計のルール
以下を参考にしたい。
https://future-architect.github.io/articles/20200409/
