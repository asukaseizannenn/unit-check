# unit-check

ユニット点検チェック用の GitHub Pages 入口ページです。

## 1. 先にGASをWebアプリとしてデプロイ
Google Apps Script 側で Webアプリをデプロイし、末尾が `/exec` のURLを取得します。

## 2. EXEC_URLを差し替える
`index.html` と `install.html` の次の行にある

```js
const EXEC_URL = '__UNIT_CHECK_GAS_EXEC_URL__';
```

を、ユニット点検チェックのGAS WebアプリURLに置き換えてください。

例:

```js
const EXEC_URL = 'https://script.google.com/macros/s/XXXXXXXXXXXXXXXX/exec';
```

## 3. GitHubへアップロード
このフォルダ内のファイルを `unit-check` リポジトリのルートへ上書きアップロードします。

## 4. GitHub Pages
GitHub の

`Settings` → `Pages`

で以下に設定します。

- Source: **Deploy from a branch**
- Branch: **main**
- Folder: **/(root)**

保存後、公開URLは通常次の形式になります。

`https://asukaseizannennn.github.io/unit-check/`

## 5. iPhone SE3
公開URLをSafariで開き、

`共有` → `ホーム画面に追加`

を選びます。

ホーム画面から起動すると、GitHub Pagesの入口からGASアプリへ自動的に移動します。

## アイコン
正式案: **チェックシート + 青いチェック + 赤リボン**

同梱:
- apple-touch-icon.png
- favicon-16x16.png
- favicon-32x32.png
- favicon-48x48.png
- favicon.ico
- icon-152.png
- icon-167.png
- icon-180.png
- icon-192.png
- icon-512.png
- icon-master-1024.png

## 注意
GitHubリポジトリはPublicのため、施設データ・利用者情報・職員情報・秘密情報は置かないでください。
このリポジトリは入口ページとアイコンのみを置く構成にします。
