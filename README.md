# 気象夏の学校 2026 サイト

GitHub Pages の静的配信だけで動くサイトです。Jekyll、Gemfile、外部ライブラリ、ビルド手順は使っていません。リポジトリをそのまま GitHub Pages に公開できます。

## 構成

- `index.html` と `*.html`
  各ページ本体です。レイアウトは共通の `assets/js/site.js` と `assets/css/style.css` で作っています。
- `content/*.md`
  各ページの本文です。基本的な文章はここだけ編集すれば反映されます。
- `data/*.csv`
  スケジュール、FAQ、リンク、招待講演などの一覧データです。
- `assets/images/`
  ポスター、人物写真、ロゴなどの画像です。
- `.nojekyll`
  GitHub Pages に Jekyll を使わせず、静的ファイルとしてそのまま配信させるためのファイルです。

## 編集場所

- トップページ本文: `content/home.md`
- ホーム上部の背景写真とタイトル文: `data/home_hero.csv`
- 開催概要の表: `data/overview.csv`
- お知らせ: `data/updates.csv`
- スケジュール: `data/schedule.csv`
- FAQ: `data/faq.csv`
- 協賛一覧: `data/sponsors.csv`
- 過去サイトリンク: `data/links.csv`
- 画像差し替え: `assets/images/`

## 注意

- Markdown 本文の中で `::updates::` や `::schedule::` のような行は、CSV を差し込むための固定記号です。削除しなければ HTML を触らずに更新できます。
- ローカルで `file://` から直接開くと、ブラウザの制限で Markdown や CSV の読み込みに失敗することがあります。GitHub Pages 上ではそのまま動きます。

## GitHub Pages で公開する手順

1. このリポジトリを GitHub に push する
2. GitHub の `Settings` → `Pages` を開く
3. `Build and deployment` で `Deploy from a branch` を選ぶ
4. Branch を `main`、Folder を `/ (root)` にする
5. 数分待つと公開 URL が発行される
