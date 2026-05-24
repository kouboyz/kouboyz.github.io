# kouboyz.github.io

松尾 宏介(Matsuo Kosuke)のプロフィールサイトです。

https://kouboyz.github.io/

## 技術スタック

- HTML
- [Tailwind CSS v4](https://tailwindcss.com/)
- Font Awesome 6（アイコン）
- Zen Kaku Gothic New（Google Fonts）
- GitHub Actions（自動デプロイ）

## ファイル構成

```
.
├── index.html
├── input.css          # Tailwind エントリーポイント
├── assets/
│   ├── output.css     # ビルド生成物（Git管理外）
│   ├── profile.png    # プロフィール画像
│   ├── badge-pmp.png  # PMP バッジ画像
│   ├── badge-cal1.png # CAL-I バッジ画像
│   └── favicon.svg    # ファビコン
├── data/
│   ├── profile.json   # 氏名・会社・bio・リンク
│   ├── talks.json     # 登壇情報
│   ├── articles.json  # 公開記事
│   └── badges.json    # 認定バッジ
└── .github/
    └── workflows/
        └── publish.yml  # GitHub Pages デプロイ
```

## コンテンツの更新

`data/` 以下の JSON ファイルを編集するだけでコンテンツを更新できます。

### talks.json

```json
{
  "title": "登壇タイトル",
  "event": "イベント名",
  "date": "YYYY-MM-DD",
  "url": "イベントページURL",
  "slidesUrl": "スライドURL（任意）",
  "videoUrl": "動画URL（任意・存在するとアイコン表示）"
}
```

### articles.json

```json
{
  "title": "記事タイトル",
  "platform": "Zenn",
  "date": "YYYY-MM-DD",
  "url": "記事URL"
}
```

### badges.json

```json
{
  "name": "バッジ名",
  "issuer": "発行元",
  "badgeUrl": "バッジページURL",
  "imageUrl": "assets/badge-xxx.png"
}
```

## ローカル開発

```bash
npm install
npm run watch   # ファイル変更を監視して自動ビルド
```

ローカルサーバーはお好みのツールで起動してください。

```bash
python3 -m http.server 8080
```

## デプロイ

`main` ブランチに push すると GitHub Actions が自動でビルド・デプロイします。

GitHub リポジトリの **Settings → Pages → Source** を **GitHub Actions** に設定してください。
