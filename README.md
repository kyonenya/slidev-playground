# slidev-playground

## PDFダウンロード

- PDFダウンロード時の [Vercelビルドエラー](https://vercel.com/kyonenya/slidev-playground/Dn8LXsJSL3ruKGowrEGbKCxwcraK) は~~Build Command を npx install playwright & npm run build にすると直った~~
  - [next.js - How to update playwright browsers in nextjs vercel? - Stack Overflow](https://stackoverflow.com/questions/73325159/how-to-update-playwright-browsers-in-nextjs-vercel) で解決に一歩近づいた
    - `"vercel-build": "slidev build && npx playwright install",`
  - 間違って deps に playwright 本体を入れていたのを消したら直った
  - 直ってない。同じく "browserType.launch: Executable doesn't exist at /vercel/.cache/ms-playwright/chromium-1060/chrome-linux/chrome" エラーが出る
    - `npx playwright install chromium`か？
      - https://github.com/microsoft/playwright/issues/18955#issuecomment-1325504987
- `canvasWidth` を 980 -> 900 に拡大したら真っ白のページができたりしたので指定しないほうがいい
- [エクスポート | Slidev](https://ja.sli.dev/guide/exporting.html)
 
## レイアウト

- [slidev/packages/client/layouts at  main · slidevjs/slidev](https://github.com/slidevjs/slidev/tree/main/packages/client/layouts)
  - ドキュメントに載ってない `two-cols-header` もある
- [Slidev デフォルトテーマのレイアウト一覧 - Zenn](https://zenn.dev/rinc5/articles/b7dc7a3b0bbd30)
- [レイアウト | Slidev](https://ja.sli.dev/builtin/layouts.html#image)

## テーマ

- [themes/packages/theme-seriph at main · slidevjs/themes · GitHub](https://github.com/slidevjs/themes/tree/main/packages/theme-seriph)
  - seriph テーマのリポジトリ
- [slidev/slides.md at main · slidevjs/slidev · GitHub](https://github.com/slidevjs/slidev/blob/main/demo/starter/slides.md)
  - seriph テーマのサンプルスライド
- [テーマを使用する | Slidev](https://ja.sli.dev/themes/use.html)
  - テーマを eject して改造する方法
- [フォントサイズ - FAQ | Slidev](https://ja.sli.dev/guide/faq.html#%E3%83%9D%E3%82%B8%E3%82%B7%E3%83%A7%E3%83%8B%E3%83%B3%E3%82%B0)
  - グローバルCSSでオーバーライドする方法

## フロントマター

- [カスタマイズ | Slidev](https://ja.sli.dev/custom/#%E3%83%95%E3%83%AD%E3%83%B3%E3%83%88%E3%83%9E%E3%82%BF%E3%83%BC%E3%81%AE%E8%A8%AD%E5%AE%9A)
