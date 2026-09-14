# personal-site

田尻慎太郎の個人サイト。HTML 1枚。ビルド不要。

- 公開先: Cloudflare Pages（`shintajiri.pages.dev`）
- 公開されるのは `public/` の中身だけ
- 更新の流れ: Claude Code に日本語で指示 → branch → PR → Cloudflare がプレビューURLをコメント → 確認 → Merge（約1分で本番）
- まずければ Cloudflare ダッシュボードで Rollback（応急）→ 取り消し PR を Merge（原本も戻す）

## Cloudflare Pages の設定値

| 項目 | 値 |
|---|---|
| Production branch | `main` |
| Build command | `exit 0` |
| Build output directory | `public` |
| Root directory | （空欄） |

## ローカル確認

```sh
cd ~/personal-site/public && python3 -m http.server 8000
# → http://localhost:8000
```

ローカルの clone は Dropbox の外（`~/personal-site`）に置く。git と Dropbox の同期は衝突するため。
計画の原本は `Dropbox/AI/personal-site/00_計画_20260915.md`。
