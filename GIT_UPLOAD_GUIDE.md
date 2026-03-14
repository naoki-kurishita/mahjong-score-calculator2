# 📤 GitHubにアップロードする方法

## 方法1: GitHub Webサイトから直接アップロード（簡単！）

### ステップ1: GitHubにログイン
1. https://github.com にアクセス
2. ログイン

### ステップ2: 新しいリポジトリを作成
1. 右上の「+」→「New repository」をクリック
2. Repository name: `mahjong-score-calculator`（好きな名前）
3. Description: `麻雀スコア計算機 - リアルタイム同期対応`
4. Public または Private を選択
5. ✅ **「Add a README file」にチェック**
6. 「Create repository」をクリック

### ステップ3: ファイルをアップロード
1. リポジトリのメイン画面で「Add file」→「Upload files」をクリック
2. 以下のファイルをドラッグ＆ドロップ:
   - `mahjong-calculator.html`
   - `manifest.json`
   - `service-worker.js`
   - （オプション）`README.md`
3. Commit message: `初回コミット: 麻雀スコア計算機`
4. 「Commit changes」をクリック

✅ 完了！

---

## 方法2: Git コマンドライン（上級者向け）

### 前提条件
- Gitがインストール済み
- GitHubアカウント作成済み

### ステップ1: ローカルでGitリポジトリを初期化

```bash
# ファイルがあるディレクトリに移動
cd /path/to/your/files

# Gitリポジトリを初期化
git init

# ファイルを追加
git add mahjong-calculator.html
git add manifest.json
git add service-worker.js

# 最初のコミット
git commit -m "初回コミット: 麻雀スコア計算機"
```

### ステップ2: GitHubにリポジトリを作成
1. https://github.com/new にアクセス
2. Repository name: `mahjong-score-calculator`
3. 「Create repository」をクリック
4. 表示されるURLをコピー（例: `https://github.com/username/mahjong-score-calculator.git`）

### ステップ3: リモートリポジトリに接続してプッシュ

```bash
# リモートリポジトリを追加
git remote add origin https://github.com/username/mahjong-score-calculator.git

# メインブランチにリネーム（必要な場合）
git branch -M main

# プッシュ
git push -u origin main
```

✅ 完了！

---

## 方法3: GitHub Desktop（GUIで簡単）

### ステップ1: GitHub Desktopをインストール
- https://desktop.github.com/ からダウンロード

### ステップ2: ファイルをリポジトリに追加
1. GitHub Desktopを起動
2. 「File」→「Add local repository」
3. ファイルがあるフォルダを選択
4. 「Create repository」をクリック

### ステップ3: GitHubにプッシュ
1. 「Publish repository」をクリック
2. Name: `mahjong-score-calculator`
3. 「Publish repository」をクリック

✅ 完了！

---

## 📋 アップロードすべきファイル

### 必須ファイル:
- ✅ `mahjong-calculator.html` - メインアプリ
- ✅ `manifest.json` - PWA設定
- ✅ `service-worker.js` - オフライン対応

### 推奨ファイル:
- ✅ `README.md` - プロジェクト説明
- ✅ `.gitignore` - 不要なファイルを除外

### 除外すべきファイル（機密情報）:
- ❌ Firebase設定ファイル（すでにHTMLに埋め込み済みなので問題なし）
- ❌ ローカル設定ファイル

---

## 📝 README.mdの例

```markdown
# 🀄 麻雀スコア計算機

簡単・正確・自動計算のリアルタイム対応麻雀スコア計算アプリ

## 特徴

- ✅ 4人麻雀のスコア自動計算
- ✅ ウマ・オカ・トビウマ対応
- ✅ チップ計算機能
- ✅ リアルタイム同期（複数人でプレイ可能）
- ✅ PWA対応（オフラインでも動作）
- ✅ モバイル最適化

## デモ

https://your-vercel-url.vercel.app

## 使い方

1. ルームを作成または参加
2. プレイヤー名を入力
3. 各回戦の点数を入力
4. 自動で計算・順位表示

## 技術スタック

- HTML/CSS/JavaScript
- Firebase Realtime Database
- PWA (Progressive Web App)

## ライセンス

MIT
```

---

## 🔒 セキュリティ注意事項

### Firebase設定について:
現在、Firebase設定がHTMLファイルに直接埋め込まれていますが、これは**一般的なWebアプリでは正常な動作**です。

**理由:**
- API Keyは公開されても問題ない（クライアント側で使用するため）
- Firebase Security Rulesで保護されている
- ドメイン制限をかけることも可能

**さらに安全にしたい場合:**
1. Firebaseコンソール → プロジェクト設定
2. 「承認済みドメイン」にVercelのURLを追加
3. 他のドメインからのアクセスを制限

---

## 🚀 次のステップ

GitHubにアップロード後:
1. ✅ Vercelと連携（自動デプロイ）
2. ✅ カスタムドメイン設定（オプション）
3. ✅ Issues/Pull Requestsで改善提案を受け付け

---

## ❓ よくある質問

**Q: プライベートリポジトリにすべき？**
A: 公開しても問題ありません。Firebase設定は公開されても安全です。

**Q: どの方法が一番簡単？**
A: 方法1（Webサイトから直接アップロード）が最も簡単です！

**Q: 更新する時はどうすれば？**
A: 同じ方法でファイルを上書きアップロードするか、`git push`します。

**Q: Vercelとの連携は？**
A: GitHubにアップロード後、Vercelで「Import Project」→GitHubリポジトリを選択

---

どの方法でアップロードしますか？サポートが必要なら教えてください！
