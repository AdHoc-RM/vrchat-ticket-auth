# vrchat-ticket-auth

VRChat ワールドのチケット認証で参照するハッシュリストの配信用リポジトリです。

- 配信 URL: https://adhoc-rm.github.io/vrchat-ticket-auth/tickets.json
- `tickets.json` は自動更新されます。手動で編集しないでください。
- このリポジトリは公開されています。コード・個人情報・秘密情報を置かないでください。

## tickets.json の形式

```json
{
  "updatedAt": "2026-10-06T00:00:00.000Z",
  "count": 0,
  "hashes": []
}
```

- `updatedAt`: 最終更新日時（UTC, ISO 8601）
- `count`: `hashes` の件数
- `hashes`: チケットごとのハッシュ（SHA-256, 16 進小文字）

## GitHub Pages の有効化手順（リポジトリ管理者向け）

Pages の設定にはこのリポジトリの管理者（Admin）権限が必要です。

1. このリポジトリの **Settings** を開く
2. 左メニューの **Pages** を開く
3. **Build and deployment** の **Source** で **Deploy from a branch** を選ぶ
4. **Branch** で `main` と `/ (root)` を選び、**Save** を押す
5. 数分後、上記の配信 URL をブラウザで開き、`"hashes": []` を含む JSON が表示されれば完了です
