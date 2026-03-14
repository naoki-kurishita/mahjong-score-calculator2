# 🀄 麻雀スコア計算機

簡単・正確・自動計算のリアルタイム対応麻雀スコア計算アプリ

## ✨ 特徴

- ✅ **4人麻雀の自動計算** - ウマ・オカを自動で計算
- ✅ **トビウマ対応** - マイナス点が出た場合も正確に計算
- ✅ **チップ計算** - チップの加算も簡単
- ✅ **リアルタイム同期** - 複数人で同じルームに参加して同時プレイ
- ✅ **点数入力の同期** - 入力中の点数が全員に表示
- ✅ **自動画面切り替え** - ゲーム開始・終了を全員に通知
- ✅ **履歴管理** - 過去の回戦を確認・編集可能
- ✅ **PWA対応** - オフラインでも動作、ホーム画面に追加可能
- ✅ **モバイル最適化** - スマホで使いやすいUI

## 🎮 デモ

https://mahjong-score-app-six.vercel.app

## 📱 使い方

### 1. ルーム作成・参加
- **ホストの場合**: 「新しいゲームを作成」→ 名前を入力 → 4桁のルームコードをシェア
- **参加者の場合**: ルームコードを入力 → 「ルームに参加」→ 名前を入力

### 2. ゲーム設定
- プレイヤー名を確認（ルーム参加時の名前が自動入力）
- ウマ・トビウマ・チップ単価を設定（リアルタイム同期）

### 3. ゲーム開始
- 誰かが「ゲーム開始」を押すと、全員の画面が自動で切り替わる

### 4. 点数入力
- 各プレイヤーの点数を入力
- マイナス点は数字入力後に `±` ボタンをタップ
- 入力中の値が全員に表示される

### 5. スコア確認
- スコアボードで現在の順位を確認
- 履歴タブで過去の回戦を確認・編集

### 6. ゲーム終了
- チップを入力して終了
- 最終結果が全員に表示される

## 🛠️ 技術スタック

- **フロントエンド**: HTML5, CSS3, JavaScript (Vanilla)
- **データベース**: Firebase Realtime Database
- **ホスティング**: Vercel
- **PWA**: Service Worker, Web Manifest

## 🚀 セットアップ

### 必要なもの
- Firebaseプロジェクト
- Vercelアカウント（デプロイ用）

### Firebase設定

1. [Firebase Console](https://console.firebase.google.com) でプロジェクトを作成
2. Realtime Database を有効化（テストモード）
3. ウェブアプリを登録して設定情報を取得
4. `mahjong-calculator.html` の Firebase設定部分を更新:

```javascript
// 🔥 Firebase設定 - ここを編集してください！
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
    databaseURL: "https://YOUR_PROJECT_ID-default-rtdb.firebaseio.com",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_PROJECT_ID.appspot.com",
    messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
    appId: "YOUR_APP_ID"
};
```

### Vercelにデプロイ

1. GitHubにプッシュ
2. [Vercel](https://vercel.com) にログイン
3. 「Import Project」→ GitHubリポジトリを選択
4. デプロイ完了！

## 📂 ファイル構成

```
mahjong-calculator/
├── mahjong-calculator.html  # メインアプリケーション
├── manifest.json             # PWA設定
├── service-worker.js         # オフライン対応
└── README.md                 # このファイル
```

## 🔐 セキュリティ

- Firebase Security Rules でデータを保護
- ルームコードによるアクセス制限
- API Keyは公開しても安全（クライアント側使用のため）

## 📝 ライセンス

MIT License

## 🤝 貢献

プルリクエスト歓迎！バグ報告や機能提案は Issues でお願いします。

## 📧 お問い合わせ

質問や提案がある場合は、Issues を作成してください。

---

**開発者**: クリシタ  
**最終更新**: 2026年2月11日
