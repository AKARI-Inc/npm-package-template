# npm-package-template

https://zenn.dev/sprout2000/books/9325fe6c9c1ba9
を基に作成。

## (開発前にやる) Git pre-commit hook set up

```bash
git config --local core.hooksPath .githooks
```


## ローカルの Node による環境構築

VSCode での快適な開発のためにも Docker を使う方もこちらの作業をおすすめします (VSCode の devcontainer の技術がある方はお知らせください)。 

まず、Node と npm をインストールします。Windows の場合は公式サイトからのダウンロードが丸いイメージ。Ubuntu の場合は[こちら](https://qiita.com/seibe/items/36cef7df85fe2cefa3ea)のように、旧バージョンの nodejs, npm を入れ、 n を一度インストールしてから、node の最新版をいれ、旧バージョンを削除するので落ち着いた。Mac はわかりません。


```bash
cd front
npm i # i stands for install
npm start
```

このあと http://localhost:3000 に接続すると、front に接続できます。


## npm パッケージのインストール

```bash
npm i hoge
```

## 開発環境でしか使わない npm パッケージのインストール

```bash
npm i -D fuga
```

で devDependencies に追加される。

[Definitely Typed](https://github.com/DefinitelyTyped/DefinitelyTyped) の TypeScrpt 型定義ファイルはこちらでインストールすること。

## ビルド

```bash
npm run build
```

## テスト

```bash
npm test
```

## カバレッジの可視化

```bash
npx http-server -o coverage/lcov-report
```
