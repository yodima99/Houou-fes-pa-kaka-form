# 鳳櫻祭2026オリジナルグッズ申込サイト（ゆらぎOFFICIAL STORE）

GitHub Pagesで即座に無料公開・動作できる完全静的Webアプリケーションです。

---

## 🚀 GitHub Pages で公開する手順（簡単2分）

### 方法A: GitHub Web画面からドラッグ＆ドロップで公開する場合

1. **GitHubでリポジトリを作成**:
   - GitHubにログインし、[新しいリポジトリを作成 (New repository)](https://github.new) します。
   - リポジトリ名（例: `bunkasai-goods`）を入力し、**Public**（公開）を選択して「Create repository」を押します。

2. **ファイルをアップロード**:
   - 「uploading an existing file」のリンクをクリックします。
   - 本フォルダ内のすべてのファイル・フォルダ（`index.html`, `styles.css`, `app.js`, `README.md`, `assets/` フォルダ）をドラッグ＆ドロップしてアップロードします。
   - 「Commit changes」を押してコミットします。

3. **GitHub Pagesを有効化**:
   - リポジトリの **「Settings」** タブを開きます。
   - 左メニューの **「Pages」** をクリックします。
   - **Build and deployment** の Source で `Deploy from a branch` を選択。
   - Branch で `main`（または `master`）/ `/ (root)` を選択して **「Save」** を押します。
4. 数十秒待つと、`https://<あなたのユーザー名>.github.io/<リポジトリ名>/` というURLが生成され、公開が完了します！

---

### 方法B: Gitコマンドで公開する場合

```bash
git init
git add .
git commit -m "Initial commit for Yuragi Official Store"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.NET.git
git push -u origin main
```

---

## 📊 Googleスプレッドシート連携（GAS）について

申込データは、GitHub Pages上から自動的に指定のGoogleスプレッドシートへ送信されます。

- **連携先スプレッドシート**: [パーカー申込状況 - Google スプレッドシート](https://docs.google.com/spreadsheets/d/1V-VU4-wJMkHqke5FzX4gnf9G9oB5yX9C9ONXuBsMdBw/edit?gid=0#gid=0)
- **送信項目**: 送信時間 / 注文ID / 商品名 / 学年 / クラス / 出席番号 / 氏名 / カラー / サイズ内訳（例: `M×1, L×1`） / 合計枚数 / 備考 / 概算金額 / ステータス

---

## 📁 構成ファイル一覧
- `index.html`: 静的HTML（GitHub Pages対応・相対パス構成）
- `styles.css`: モダンダーク/ホワイト切換レスポンシブCSS
- `app.js`: 注文処理・自動画像スライダー・GAS非同期通信
- `assets/`: 商品画像フォルダ (`sweatshirt.jpg`, `hoodie_white_bg.jpg`)
