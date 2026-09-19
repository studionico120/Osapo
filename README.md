# 公開サイト (GitHub Pages 用) — B3

App Store 申請に必須の Support / Privacy URL を満たすための静的サイト一式。
`docs/legal/` の本文を忠実に HTML 化したもの。**このディレクトリの中身を GitHub Pages リポジトリ (`Osapo`) にそのままコピーして公開する。**

## ファイル

| ファイル | 用途 | 公開 URL (studionico120 / Osapo) |
|---|---|---|
| `index.html` | Marketing (任意) | `https://studionico120.github.io/Osapo/` |
| `support.html` | **Support (必須)** | `https://studionico120.github.io/Osapo/support.html` |
| `privacy.html` | **Privacy Policy (必須)** | `https://studionico120.github.io/Osapo/privacy.html` |
| `terms.html` | 利用規約 | `https://studionico120.github.io/Osapo/terms.html` |
| `tokushoho.html` | 特定商取引法に基づく表記 | `https://studionico120.github.io/Osapo/tokushoho.html` |
| `style.css` | 共通スタイル | — |

## 差し替え状況 (2026-09-19)

| 項目 | 値 | 状態 |
|---|---|---|
| 問い合わせメール | `studionico120@gmail.com` (全ページ mailto リンク) | ✅ 反映済み |
| 販売事業者 / 運営者名 | `studionico120` | ✅ 反映済み |
| 運営責任者名 | `studionico120` | ✅ 反映済み |
| `{{app_store_url}}` | (index.html の HTML コメント内) | ⏳ App Store 公開後に差し替え |

公開前に手で埋める必須プレースホルダは**もう残っていない** (`{{app_store_url}}` は公開後で可・コメント内なので表示に影響なし)。

> ⚠️ **特商法の注意**: 販売事業者 / 運営責任者を屋号 (`studionico120`) のみで表記している。個人事業主の場合、特定商取引法は原則として**実名の表示**を求めるため、屋号のみは要件を完全には満たさない可能性がある。「所在地」「電話番号」は「請求があった場合に遅滞なく開示」としている (プラットフォーム経由のデジタル販売では一般的な運用)。**将来的には開示代行サービスの利用や行政書士への確認を推奨**。

## 公開手順 (GitHub Pages)

1. GitHub で `Osapo` リポジトリ (Public) を用意する
2. このディレクトリの `*.html` と `style.css` をリポジトリのルートに置く
3. プレースホルダを実値に置換 (上記)
4. `Settings > Pages` で Source を `main` ブランチ / `/ (root)` に設定 → 数分で公開
5. 5 つの URL がブラウザ (できれば iPhone) で開けることを確認

## App Store Connect への入力

| フィールド | URL |
|---|---|
| App Information > Support URL | `https://studionico120.github.io/Osapo/support.html` |
| App Information > Privacy Policy URL | `https://studionico120.github.io/Osapo/privacy.html` |
| App Information > Marketing URL (任意) | `https://studionico120.github.io/Osapo/` |

## 公開後 (任意)

- `index.html` の「まもなく公開」ノートを、App Store のダウンロードリンク / バッジに差し替える (`{{app_store_url}}` のコメント参照)
- 本文は `docs/legal/` が出典。法的文言を更新したら、こちらの HTML も同期すること
