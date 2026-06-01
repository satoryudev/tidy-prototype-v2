# tidy-prototype-v2

**Tidy v2** — 信頼できるAIファイル整理アシスタントの Web プロトタイプ（プロダクトデモ）。

> ⚠️ **このリポジトリはデモ（UIシミュレーション）です。実際のAPIやファイルシステムは使っていません。**
> ボタンの動きはすべてブラウザ内の演出です。実際にファイルを安全に整理する**本物の実装**は
> [**dir-organizer**](https://github.com/satoryudev/dir-organizer)（Claude Code スキル）の方です。

- 🌐 デプロイ: https://tidy-prototype-v2.vercel.app
- 🤖 本物の実装: https://github.com/satoryudev/dir-organizer
- 🏫 由来: 千葉工業大学「web3・AI概論 2026」第6回課題（プロトタイプ v2）

## v1 → v2 の核心

v1 は「見た目だけの mock」だった。v2 は価値を **「賢さ」より「信頼」** に置く：

- **削除しない** — 不要・重複ファイルはゴミ箱ではなく `_捨て/` へ隔離
- **見せてから動く** — 実行前に必ずプレビュー（dry-run）
- **全部戻せる** — 全操作を manifest に記録し undo（中断耐性あり）
- **中身を見て分類 / 複数の場所から集約 + 重複排除**
- **assess** — コードプロジェクトやシステム配下は「触らない」と判定して止める

## 構成

静的 HTML + Vanilla JS の単一ファイル（`index.html`）。バックエンドなし。Vercel に静的デプロイ。

```bash
# ローカルで開く
open index.html

# デプロイ（Vercel）
vercel --prod
```

## ライセンス

MIT
