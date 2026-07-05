# Kazuya式ダイエット逆算 PWA

食った分だけ動く、Kazuya式ダイエットアプリ。

## ファイル構成
- `index.html` - メインのアプリ画面
- `manifest.json` - PWAマニフェスト
- `service-worker.js` - オフライン対応
- `icon-192.png`, `icon-512.png` - アプリアイコン

## GitHub Pagesへのデプロイ手順

1. GitHubでリポジトリ作成（例: `diet-balance`）
2. このフォルダ内の全ファイルをコミット＆プッシュ
3. Settings → Pages → Source: `main` branch / root
4. 数分待つと `https://USERNAME.github.io/diet-balance/` で公開される

## iPhoneでのインストール手順

1. Safariで公開URLを開く
2. 共有ボタン（□↑）をタップ
3. 「ホーム画面に追加」を選択
4. アイコンがホーム画面に追加される

## Gemini API キーの取得

1. https://aistudio.google.com/apikey にアクセス
2. 「Get API key」をクリック
3. 取得したキーをアプリの設定画面に入力

## 注意事項

- APIキーはブラウザのlocalStorageに保存されます（プロトタイプ用途）
- 本格運用時はCloudflare Worker等でキー隠蔽を推奨
- Service Workerが効くのはHTTPS環境のみ（localhost含む）

## ローカルテスト

```bash
cd diet_pwa
python3 -m http.server 8000
```
http://localhost:8000 でアクセス
