# npm-package-template

https://zenn.dev/sprout2000/books/9325fe6c9c1ba9
を基に作成。

## (開発前にやる) Git pre-commit hook set up

```bash
git config --local core.hooksPath .githooks
```

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
