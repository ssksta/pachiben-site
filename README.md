# pachiben-site

iOS アプリ「ぱちベン」の紹介・サポート・プライバシーポリシーを公開するサイト。
GitHub Pages (Jekyll + minima) で配信する。**アプリ本体のソースは別リポジトリ (private) にあり、
ここにはサイトの文面だけを置く**。

公開 URL: https://ssksta.github.io/pachiben-site/

| ページ | ファイル | 用途 |
| --- | --- | --- |
| 紹介 (トップ) | `index.md` | アプリの説明。App Store Connect の「マーケティング URL」 |
| プライバシーポリシー | `privacy.md` | App Store Connect の「プライバシーポリシー URL」 (審査必須) |
| サポート / お問い合わせ | `support.md` | App Store Connect の「サポート URL」兼、権利者からの修正・削除依頼の窓口 (審査必須) |

## 更新のしかた

Markdown を直して `main` に push すれば GitHub Pages が自動で build・配信する。
ページを増やすときは `.md` を足し、`_config.yml` の `header_pages` に1行加える
(課金を入れるときの特定商取引法に基づく表記ページなど)。

ローカルで見たいときは (任意):

```bash
bundle install
bundle exec jekyll serve   # http://127.0.0.1:4000/pachiben-site/
```

## 掲載してよいもの / いけないもの

アプリ本体の権利・法令方針 (`doc/legal_considerations.md`) がそのまま効く。

- **可**: 自作アプリのスクリーンショット (機種名は通常フォントの文字表示)、アプリアイコン
- **不可**: 筐体写真・盤面画像・液晶のスクリーンショット、機種ロゴ・作品ロゴ、版権キャラクター
- **紹介ページに機種名を並べて集客 (SEO) を狙わない**。非公式アプリが版権作品名を集客に使う形になる

## 文面の根拠

- 非公式アプリの注記は `doc/legal_considerations.md`「非公式アプリであることの明示」の文面をそのまま使う
  (要約・言い換えをしない)
- プライバシーポリシーの事実関係 (依存パッケージ・外部通信は機種カタログの取得のみ・記録は端末内保存) は
  アプリ本体の Issue #420 で確認済み。**アプリの依存や通信が変わったら文面も直す**
