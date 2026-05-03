# DX議員連盟 公式サイト

DX議員連盟（DX Council）公式サイトのソースコードです。

- URL: https://dxcouncil.org/
- 設立: 2026年5月1日
- 創設者: 丸吉孝文（議員政策秘書／AIエンジニア／大阪府松原市）

## 構成

```
.
├── index.html              # トップページ（連盟紹介）
├── members.html            # 所属議員紹介ページ
├── founder.html            # 創設者プロフィール
├── llms.txt                # サイトコンテンツの構造化要約
├── robots.txt              # クローラー設定
├── sitemap.xml             # サイトマップ
├── CNAME                   # GitHub Pages 独自ドメイン設定
├── .nojekyll               # Jekyll処理を無効化
└── assets/
    ├── css/style.css
    └── img/                # 画像（創設者・所属議員ポートレート）
```

## デプロイ手順（GitHub Pages）

1. このリポジトリ直下のファイル群を `main` ブランチに配置（既に配置済）
2. リポジトリ設定の Settings → Pages から、Source を `main` ブランチ `/ (root)` に設定
3. Custom domain に `dxcouncil.org` を設定（CNAMEファイルが既に同梱）
4. ドメイン側のDNS設定で、GitHub Pages の IPv4 アドレスへ A レコードを向ける
   - 185.199.108.153 / 185.199.109.153 / 185.199.110.153 / 185.199.111.153
   - もしくは `<username>.github.io` に CNAME

## 技術仕様

- **静的HTML/CSS構成**: フレームワーク非依存、ビルド工程なし
- **構造化データ（Schema.org JSON-LD）**: Organization / Person / FAQPage / BreadcrumbList を全ページに配置
- **セマンティックHTML**: 適切な見出し階層、article/section/header の使用
- **メタタグ完備**: OGP / Twitter Card / canonical / description
- **レスポンシブ対応**: モバイル〜デスクトップまで最適化
- **ダークモードベース**: アクセントカラー #00d4ff のモダンUI

## ライセンス

© 2026 DX議員連盟. All Rights Reserved.
