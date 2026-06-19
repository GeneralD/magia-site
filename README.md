# Magia — Landing Site

![Astro](https://img.shields.io/badge/Astro-BC52EE?logo=astro&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS%20v4-06B6D4?logo=tailwindcss&logoColor=white) ![Cloudflare Workers](https://img.shields.io/badge/Cloudflare%20Workers-F38020?logo=cloudflare&logoColor=white) ![deploy](https://img.shields.io/badge/deploy-Workers%20Builds-F38020) ![status](https://img.shields.io/badge/output-static-22C55E)

[**Magia**](https://github.com/GeneralD/Magia)（究極のカスタマイズ性と処理速度を誇る、プロのための NFT ジェネレーター）の公式ランディングページです。

🔗 **Live:** _デプロイ後に更新_

---

## 技術スタック

- **[Astro](https://astro.build)** — 静的サイト生成（ゼロ JS 出力）
- **[Tailwind CSS v4](https://tailwindcss.com)** — CSS ファーストのデザイントークン
- **[Cloudflare Workers](https://developers.cloudflare.com/workers/static-assets/)** — 静的アセットをエッジ配信
- デザインは **ui-ux-pro-max**（Dark Mode OLED / web3）に基づいて構築

## 開発

```sh
bun install        # 依存をインストール
bun run dev        # 開発サーバー（http://localhost:4321）
bun run build      # dist/ にビルド
bun run preview    # ビルド結果をローカルプレビュー
```

## デプロイ

`main` への push で **Cloudflare Workers Builds** が自動ビルド・デプロイします（`bun.lock` を検出し `bun run build` を実行）。手動デプロイは次の通り:

```sh
bun run build
wrangler deploy
```

## 構成

```text
src/
├── layouts/Layout.astro      # <head>・フォント・メタ
├── components/               # Nav / Hero / Features / HowItWorks / Showcase / Install / Footer
├── pages/index.astro         # ランディングページ本体
├── pages/404.astro           # 404
└── styles/global.css         # デザイントークン（@theme）・エフェクト

wrangler.jsonc                # Cloudflare 静的アセット設定
```

---

> Magia 本体は [GeneralD/Magia](https://github.com/GeneralD/Magia) を参照。
