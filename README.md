# Splender Viewer

宝石の煌めき (Splendor) の感想戦ビューア。GitHub Pages で配信するアプリの外殻だけを置く公開リポジトリ。

- 配信URL: https://raidq222.github.io/splender-viewer/
- **棋譜・対局データ・個人情報は一切含まない** (同梱棋譜は空でビルドしてある)。
  対局データは別のprivateリポジトリにだけ置く
- 中身は単一HTML (`gh-pages` ブランチの `index.html`)。
  ビルド元は private リポジトリの `vite.pages.config.ts` (`npx vite build --config vite.pages.config.ts`)
- 用途: BGAのユーザースクリプトが対局終了直後に `window.open` でこのページを開き、
  `postMessage` で棋譜を渡すと、その場で感想戦が自動で開く。
  受け口は `boardgamearena.com` オリジンからのメッセージだけを受け付ける
- 更新は週次の自動分析ルーチンが行う (push前に個人データが無いことをgrepで確認する手順つき)
