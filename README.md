# 漢字から中国語 Website

日本語の漢字知識を活かして中国語を学ぶiPhoneアプリの公式サイトです。
HTMLとCSSのみの静的サイトです。外部依存、ビルド工程、JavaScript、Webフォント、アクセス解析はありません。

## Production URL

https://hmnuiodaryim0-lab.github.io/kanjikarachinese-site/

## Pages structure

```text
index.html                   ホーム
privacy/index.html           プライバシーポリシー
support/index.html           サポート
assets/css/styles.css        共通スタイル
assets/images/app-icon.png   正式App Icon（1024 × 1024）
assets/images/app-icon-180.png
assets/images/app-icon-512.png
robots.txt
sitemap.xml
.nojekyll
.gitignore
README.md
```

ナビゲーションは画面幅に合わせて折り返し、FAQはHTMLのdetails要素を使用しています。JavaScriptは不要です。

## Local preview

このディレクトリで実行します。

```sh
python3 -m http.server 8080
```

http://localhost:8080 を開きます。確認後は `Ctrl+C` で終了します。

## Deployment

GitHub Pages: **main branch / root (/)**

`main`へpushするとGitHub Pagesで公開されます。内部リンクはプロジェクトのサブパスでも利用できる相対URLです。

Repository: https://github.com/hmnuiodaryim0-lab/kanjikarachinese-site

## App Store URLの更新

`index.html`内の `APP_STORE_URL` コメントを検索してください。CTAはこの1か所だけです。
正式URLが公開されたら、直後のdisabledボタンを以下の形式のリンクに置き換えます。
`OFFICIAL_APP_STORE_URL`を実際のURLに置き換えてから公開してください。

```html
<a class="store-button" href="OFFICIAL_APP_STORE_URL">App Storeでダウンロード</a>
```

架空のURL、価格、評価は設定していません。

## App Icon

App工程の `Assets.xcassets/AppIcon.appiconset/Contents.json` で指定されたDefault / Anyの
`AppIcon-1024.png`を、そのまま `assets/images/app-icon.png`へコピーしています。
180pxと512px版はmacOSの`sips`でリサイズしています。元のApp工程は変更していません。

## Support / Privacy

問い合わせ先はGitHub Issuesです（GitHubアカウントが必要、投稿は公開）。
サイトに開発者独自のAnalytics、広告、Cookie、Trackingはありません。
GitHub Pages側の技術情報の処理についてはプライバシーページから公式方針を参照できます。

## Metadata

各ページにHTTPS canonical、description、Open Graph、Twitter summaryを設定しています。
ホームにSoftwareApplication JSON-LD、サイトにsitemap.xmlとrobots.txtを配置しています。
価格・評価・レビュー数は未確定のため掲載していません。
