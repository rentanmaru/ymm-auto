# GitHub Pages 公開手順

このディレクトリの3ファイルを GitHub Pages 経由で公開して、TikTok Developer 申請に使う。

## 手順 (5分)

1. **GitHub で新規リポジトリ作成**
   - リポジトリ名: `ymm-auto`  (推奨、URLが `https://rentanmaru.github.io/ymm-auto/` になる)
   - 公開設定: **Public** (Privateだとページ公開不可)
   - README作成: 不要 (既存のindex.htmlがあるため)

2. **このディレクトリの中身をリポジトリへPush**
   ```powershell
   cd "f:\Claude project\YMM_auto\_tiktok_site"
   git init
   git add index.html privacy-policy.html terms-of-service.html
   git commit -m "Initial: YMM Auto Uploader site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/ymm-auto.git
   git push -u origin main
   ```

3. **GitHub Pages 有効化**
   - リポジトリページ → **Settings** → **Pages**
   - Source: **Deploy from a branch**
   - Branch: **main** / Folder: **/ (root)**
   - Save → 1〜2分でURL表示

4. **動作確認**
   - `https://<your-username>.github.io/ymm-auto/index.html` をブラウザで開く
   - ナビゲーションから Privacy Policy / Terms of Service にアクセスできることを確認
   - TikTok審査では3つすべてのURLを使う

## TikTok Developer Portal で使うURL

| 項目 | URL |
|---|---|
| Website URL | `https://<username>.github.io/ymm-auto/` |
| Privacy Policy URL | `https://<username>.github.io/ymm-auto/privacy-policy.html` |
| Terms of Service URL | `https://<username>.github.io/ymm-auto/terms-of-service.html` |

## カスタマイズ

- メールアドレス: 全3ファイルで `rentanmaru2005@gmail.com` を使用 (変更する場合は3箇所)
- アプリ名: `YMM Auto Uploader` を別名にする場合は3ファイルで修正
- 色: CSS の `#c00` (赤) を変更すれば配色変更可

## 注意

- Privateリポジトリでは GitHub Pages 公開不可 (Pro/Enterprise プランのみ)
- カスタムドメインを使いたい場合は Settings → Pages → Custom domain で設定可能
